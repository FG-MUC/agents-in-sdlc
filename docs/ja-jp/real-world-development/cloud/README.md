---
slug: ja-jp/real-world-development/cloud
title: "GitHub Copilot クラウドエージェント"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

[**GitHub Copilot クラウドエージェント**](https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent)を使うと、GitHub Copilot がクラウドで非同期に作業できます。GitHub で作業を割り当てると、クラウドエージェントがバックグラウンドでリポジトリを調査し、変更を行い、プルリクエストを作成します。その間、別の作業を続けられます。

この演習では、クラウドエージェントが従うカスタム指示を追加し、GitHub issue を割り当てて実装を依頼します。カスタムエージェントを確認してそのアプローチを調整し、エージェント ダッシュボードからセッションの進捗を監視して方向付けます。最後に、作成されたプルリクエストをレビューし、結果を反復的に改善します。

## 演習

| 演習 | トピック | 説明 |
|----------|-------|-------------|
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成する |
| [1. カスタム指示][ex1] | コンテキスト | クラウドエージェントが従うカスタム指示を追加する |
| [2. クラウドエージェント][ex2] | 非同期エージェント | Copilot クラウドエージェントに issue を割り当てる |
| [3. カスタムエージェント][ex3] | 専門エージェント | カスタムエージェントを確認して使用する |
| [4. エージェントの管理][ex4] | 監視 | エージェントセッションを監視して方向付ける |
| [5. 反復][ex5] | レビュー | プルリクエストをレビューし、Copilot の作業を反復し、次の手順を選択する |

## 前提条件

このワークショップに参加する前に、次のものを用意してください。

- [ ] 有効な **Copilot Student、Pro、Pro+、Business、Enterprise** プランの GitHub アカウント
- [ ] アカウントまたは組織で有効になっている Copilot クラウドエージェント

> [!TIP]
> 有料プランをお持ちでない場合、学生として認証された方は[GitHub Education][callout-student-plan-education]を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使うエージェント、Model Context Protocol (MCP)、コードレビュー、Copilot CLI の機能が含まれているため、どの環境でも最後まで進められます。

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> クラウドエージェントは **Copilot Student、Pro、Pro+、Business、Enterprise** で利用できます。Copilot Free は対象外です。Copilot Business または Enterprise では、管理者が組織で有効にする必要があります。

> [!NOTE]
> この環境では MCP を扱いません。Copilot で MCP サーバーを使う方法については、[CLI 環境][cli]または [VS Code 環境][vscode]を参照してください。

## 始める

**[演習 0: 前提条件から始める →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-custom-instructions/
[ex2]: 2-cloud-agent/
[ex3]: 3-custom-agents/
[ex4]: 4-managing-agents/
[ex5]: 5-iterating/
[cli]: ../cli/
[vscode]: ../vscode/
