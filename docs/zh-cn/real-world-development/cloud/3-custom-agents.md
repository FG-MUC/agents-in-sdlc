---
title: "练习 3：自定义代理"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

## 什么是自定义代理？

GitHub Copilot 中的[自定义代理][custom-agents-concept]可以创建专门处理开发工作流中特定任务或领域的 AI 助手。通过在仓库的 `.github/agents` 文件夹中定义 Markdown 文件，你可以为 Copilot 提供有针对性的指令、最佳实践、编码模式和领域知识。团队可以将专业经验整理为可复用的代理，例如确保符合 [WCAG][wcag] 标准的无障碍代理、遵循安全编码实践的安全代理，或保持测试模式一致的测试代理。

自定义代理通过项目 `.github/agents` 文件夹中的 Markdown 文件定义，也可以在全局路径 `~/.copilot/agents` 中定义。每个文件都包含 YAML frontmatter，至少需要 `name` 和 `description` 字段；之后是定义代理行为、专业知识和指令的 Markdown 提示。

### 自定义代理与代理技能

自定义代理和[代理技能][agent-skills-concept]有些相似之处。两者主要通过 Markdown 文件定义，用于告诉 AI 如何执行任务。最简单的区分方式是：**自定义代理负责执行工作，技能则是工具**。

自定义代理拥有自己的上下文窗口，并且可以在工作中协调技能，甚至协调其他代理。在本练习中，无障碍自定义代理会依据无障碍指南审查和更新网站；它可以在此过程中调用拉取请求工作流技能或用于运行和管理测试的技能。

> [!NOTE]
> 编写自定义代理没有唯一的正确方式。与其他 AI 功能一样，请不断测试和迭代，找到适合你的环境和场景的方式。

[custom-agents-concept]: https://docs.github.com/copilot/concepts/agents/cloud-agent/about-custom-agents
[agent-skills-concept]: https://docs.github.com/copilot/concepts/agents/about-agent-skills
[wcag]: https://www.w3.org/WAI/standards-guidelines/wcag/

在本练习中，你将了解：

- 如何定义自定义代理。
- 如何向自定义代理分配任务。

## 场景

Tailspin Toys 致力于让所有人都能使用其众筹平台，不受视觉能力或偏好的影响。近期用户反馈指出，由于文字和背景颜色的对比度不足，有些用户难以阅读当前的深色主题。为解决此无障碍问题，设计团队要求实现可由用户切换的高对比度模式。

无障碍功能至关重要，因此你希望尽快实现它。你将使用自定义代理生成此功能。

## 审查无障碍自定义代理

我们已为你创建了无障碍自定义代理。请审查其内容，了解它将如何指导 Copilot。

返回 Codespace，然后审查无障碍自定义代理文件：

1. 打开 `.github/agents/accessibility.md`。
2. 查看 YAML frontmatter 中的 `name` 和 `description` 字段。

> [!CAUTION]
> 自定义代理必须包含带有 `name` 和 `description` 的 frontmatter。

3. 阅读后续部分，了解以下内容：
   - 为无障碍网站生成代码时的核心职责。
   - 无障碍最佳实践。
   - HTML、CSS 和 JavaScript 代码示例。
   - 常见问题和错误。

## 创建并分配议题

代理控制台是管理开发环境中所有代理的中心位置。你可以将任务分配给 Copilot 云代理、监控任务，甚至引导进行中的会话。现在将创建高对比度模式的任务分配给 Copilot。

1. 转到你的仓库。
2. 选择 **Issues** 选项卡。
3. 选择 **New issue** 打开新议题对话框。
4. 选择 **Blank issue** 创建新议题。
5. 在 **Title** 中输入 `Add high contrast mode to website`。
6. 在 **Description** 中输入：

    ```plaintext
    We need a high contrast mode for the site. There should be a toggle for high contrast which the user can set. It should store the setting in local storage on the browser.
    ```

7. 选择 **Create** 创建议题。
8. 在右侧选择 **Assign to Copilot**，打开分配对话框。
9. 从自定义代理列表中选择 **Accessibility agent**。

    ![云代理分配截图，其中高亮显示了 Accessibility 自定义代理](../../../_images/ex5-select-custom-agent.png)

10. 选择 **Assign**。
11. Copilot 随即在后台开始工作。

## 总结和后续步骤

本课程介绍了 GitHub Copilot 中的[自定义代理][custom-agents]，也就是专门处理特定任务和领域的 AI 助手。使用自定义代理可以将团队的专业知识和标准整理为可复用的代理，更有效地指导 Copilot 完成相应工作。

你了解了以下概念：

- 如何定义自定义代理。
- 如何向自定义代理分配任务。

Copilot 正在实现高对比度模式。接下来，你可以在代理控制台中[监控并引导代理会话][next-lesson]。

## 资源

- [关于自定义代理][custom-agents]
- [为组织使用自定义代理做好准备][org-custom-agents]
- [为企业使用自定义代理做好准备][enterprise-custom-agents]

---

| [← 上一课程：GitHub Copilot 云代理][previous-lesson] | [下一课程：监控和管理代理 →][next-lesson] |
|:--|--:|

[previous-lesson]: ../2-cloud-agent/
[next-lesson]: ../4-managing-agents/
[custom-agents]: https://docs.github.com/copilot/concepts/agents/cloud-agent/about-custom-agents
[org-custom-agents]: https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-organization/prepare-for-custom-agents
[enterprise-custom-agents]: https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-agents/prepare-for-custom-agents
