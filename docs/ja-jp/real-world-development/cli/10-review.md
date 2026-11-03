---
title: "レッスン 10: 振り返りと次のステップ"
description: "Copilot CLI のワークフロー、2 つのプルリクエスト、再利用可能なカスタマイズ、追加リソースを振り返ります。"
authors:
  - geektrainer
lastUpdated: 2026-09-29
---

Tailspin Toys の一連のワークフローで GitHub Copilot CLI を使用しました。次の操作を行いました。

- Codespace を準備し、Copilot CLI をインストールし、プロジェクトを確認して、用意されていたフィルター issue を見つけました。
- 星評価を追加し、転送ブラウザーで結果を確認して、最初のプルリクエスト (PR) を手動でマージしました。
- フィルター issue から始め、Plan モードでアプローチを決め、Autopilot モードで実装し、Interactive モードでレビューしました。
- カスタム指示でエージェントを導き、既存の `quality-checks` スキルをカスタマイズして、ユニット テスト、lint、型チェックを実行しました。
- Playwright Model Context Protocol (MCP) サーバーを追加し、実際のブラウザーでフィルター機能を確認しました。
- 品質保証 (QA) カスタム エージェントを作成して選択し、要件、テスト カバレッジ、スキルの結果、ブラウザーでの確認結果を評価させました。
- フィルター機能の変更全体をレビューし、その PR に Agent Merge を許可しました。
- コンテキスト、モデル、共有、任意のクラウドへの委任に使うスラッシュコマンドを確認しました。

## 作成したもの

このワークショップには、更新した `main` からそれぞれ独自のブランチを作成する、2 つの PR の節目があります。

1. **星評価:** 既存の `starRating` と未評価状態をゲームカードに表示します。
2. **フィルターと品質ワークフロー:** フィルター機能を実装し、指示を更新して機能に適用します。`quality-checks` レポートをカスタマイズし、QA プロファイルを作成して、関連するテストを追加します。

フィルターの計画から PR の作成まで、同じ会話とブランチを使用しました。ワークショップを簡潔に進めるため、この作業を 1 つの PR にまとめました。

## さまざまな検証方法

自動テスト、自分でのブラウザー確認、MCP 経由の Copilot によるブラウザー操作でコードを確認しました。`quality-checks` スキルはユニット テスト、lint、型チェックを実行し、新しい形式で報告しました。PR の前に QA が、要件とテスト カバレッジのレビューをこれらの結果とまとめました。

追加したテストは実際の不足を補うものである必要があります。QA の実行で新しいテストが不要と判断されることもあります。マージを許可する前にコードと証拠をレビューし、変更後は影響を受ける検証をやり直してください。

## ベスト プラクティス

Copilot に与えるコンテキストとツールが、作業の結果を左右します。このワークショップでは、指示を更新し、スキルをカスタマイズし、QA プロファイルを作成し、MCP サーバーを構成しました。これらのカスタマイズを会話間で再利用し、チームのニーズに合わせて調整してください。指示は標準を設定し、スキルは繰り返し可能なタスクを説明し、カスタム エージェントは専門的な役割を定義し、MCP サーバーは外部ツールに接続します。エージェントの概要だけでなく、実際の変更とツールの結果を確認してください。

タスクに合った**モードとモデル**を選びます。実装前の検討には **Plan**、範囲の狭い変更で常に確認しながら進めるには **Interactive**、範囲の明確なタスクには **Autopilot** を使います。定型的な編集には高速なモデルを、複雑な作業にはより高性能なモデルを選びます。

インフラと同じくらい、コンテキストも重要です。作りたいもの、理由、方法を明確に説明すると、結果が大きく変わります。

## さらに確認する

主要なワークフローを終えました。Copilot CLI には、ほかにも次の機能があります。

- `/review` でコードレビュー エージェントに変更を分析させる。
- `/rubber-duck` で問題を説明し、別の視点を得る。
- `/fleet` で独立したサブタスクを並行して調整する。
- `/worktree` で別のタスクを分離する。
- `/delegate` で Copilot クラウドエージェントにタスクを送信する。

## 次のステップ

どのツールでも、上達する最善の方法は使い続けることです。実稼働コード、趣味のコード、何年も作りたいと思っていた小さなアプリなどで活用してください。学んだことをチームと共有し、ほかのメンバーからも学びましょう。そして、ドキュメントも確認してください。

ターミナルから Tailspin Toys を拡張する場合は、任意の [Foundry Backer Concierge シリーズ][foundry]に進みます。ほかの環境を比較するには、[VS Code ワークショップ][vscode]、[GitHub Copilot アプリのワークショップ][app]、または [Copilot クラウドエージェントのワークショップ][cloud]を確認してください。

## リソース

- [GitHub Copilot CLI について][about-cli]
- [Copilot CLI コマンド リファレンス][cli-reference]
- [Copilot CLI のカスタマイズ][customize-cli]
- [Copilot CLI でプルリクエストを管理する][manage-prs]

[previous-lesson]: ../9-cli-power-tools/
[foundry]: ../8-foundry-agent/
[vscode]: ../../vscode/
[app]: ../../app/
[cloud]: ../../cloud/
[about-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[customize-cli]: https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
