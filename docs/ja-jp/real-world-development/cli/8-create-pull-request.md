---
title: "レッスン 8: 機能のプルリクエストを作成してマージする"
description: "フィルター機能、指示、スキルの更新、QA プロファイル、テストをまとめてレビューし、プルリクエストを作成して Agent Merge を使用します。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

フィルター機能の実装、指示の更新、スキルの更新、品質保証 (QA) プロファイル、テストはすべて 1 つのブランチに保存されています。これらをまとめてレビューし、プルリクエストを作成します。星評価のプルリクエスト (PR) は自分でマージしましたが、今回は **Agent Merge** にプロセスを管理させます。

> [!NOTE]
> 通常は、機能、指示、スキル、QA エージェントを複数の PR に分けます。ワークショップを簡潔に進めるため、フィルター機能と品質ワークフロー全体を 1 つの会話とブランチにまとめ、1 つの PR に含めます。

このレッスンでは、次の操作を行います。

- Agent Merge と、マージ ライフサイクルを自動化する方法を学びます。
- 機能の変更全体と検証結果を確認します。
- フィルター機能の PR を作成します。
- レビュー後にのみ Agent Merge を有効にし、PR がマージされたことを確認します。

## シナリオ

フィルター機能のワークフロー全体で、Copilot を使って機能の計画、実装、検証を行いました。Tailspin Toys は、マージの承認を開発者が管理したまま、PR に関する残りの作業を自動化したいと考えています。

## Agent Merge とは

**Agent Merge** は、プルリクエストを取り込むために必要な残りの作業を自動化します。有効にすると、Copilot は PR のブロック要因に対応します。失敗した継続的インテグレーション (CI) チェックの修正、レビュー コメントへの対応、必要に応じたリベースを行い、リポジトリで許可されていれば GitHub の自動マージを有効にします。

これまでは自分で **Merge pull request** を選択していました。Agent Merge にその作業を任せることもできます。Agent Merge を有効にする前に、変更をレビューして準備ができていることを確認してください。

## Agent Merge で PR を管理する

コードの作成が終わったら、全体をレビューし、PR を作成して、残りのプロセスを Agent Merge に任せましょう。

1. Codespace に戻ります。
2. `/agent` を入力してエージェント ダイアログを開きます。
3. 選択肢から **Default** を選び、<kbd>Enter</kbd> を押します。
4. `/pr create` コマンドで新しい PR を作成します。
5. `/pr agentmerge` を実行して Agent Merge を有効にします。
6. Copilot が PR の継続的インテグレーションを監視します。すべて成功すると、マージを実行します。
7. 「PR #14 was squash-merged successfully」のようなメッセージが Copilot から表示されることを確認します。

> [!IMPORTANT]
> Agent Merge は、必須の承認、ブランチ保護、マージ キュー、リポジトリ設定、権限の不足を回避しません。ブロックされた場合は理由を確認し、リポジトリで許可されていれば、レビュー済みの PR を手動でマージします。

## まとめと次のステップ

コードの生成、テストと検証、プルリクエストのプロセスなど、開発プロセスの複数の部分を自動化しました。具体的には、次の操作を行いました。

- Agent Merge と、マージ ライフサイクルを自動化する方法を学びました。
- 機能の変更全体と検証結果を確認しました。
- フィルター機能の PR を作成しました。
- レビュー後にのみ Agent Merge を有効にし、PR がマージされたことを確認しました。

次は、コンテキスト、モデル、共有、任意のクラウドへの委任に使える[便利な Copilot CLI スラッシュコマンド][next-lesson]を確認します。

## リソース

- [Copilot CLI でプルリクエストを管理する][manage-prs]
- [Copilot CLI コマンド リファレンス][cli-reference]

[previous-lesson]: ../7-qa-agent/
[next-lesson]: ../9-cli-power-tools/
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
