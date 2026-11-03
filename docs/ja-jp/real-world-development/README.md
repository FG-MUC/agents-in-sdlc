---
title: "実践的な開発"
slug: ja-jp/real-world-development
authors:
  - geektrainer
lastUpdated: 2026-09-16
---

現実的なシナリオ、完成したアプリケーション、共有バックログを使って、ソフトウェア開発ライフサイクル全体で GitHub Copilot を活用します。変更の計画、コードの作成、動作のテスト、プルリクエストのレビュー、エージェントによる作業の管理を繰り返しながら進めます。

## シナリオ

架空の企業 Tailspin Toys に新しく加わった開発者として作業します。同社は開発者をテーマにしたボードゲームのクラウドファンディングを運営しています。チームのバックログは GitHub issue として登録済みで、すぐに着手できます。フィルターやページネーションなどの機能開発に加えて、アクセシビリティやコーディング規約などの品質改善も含まれています。

## 開発環境を選ぶ

GitHub Copilot は、どの環境でも利用できます。開発方法に合った環境を選んでください。各ワークショップはそれぞれの環境設定から始まり、共通の Tailspin Toys シナリオを使います。

### [GitHub Copilot CLI][cli]

ターミナルでエージェントアシスタントを使用します。Plan モードと Autopilot モード、指示、スキル、カスタムエージェント、Playwright の Model Context Protocol (MCP) サーバー、Agent Merge、便利なスラッシュコマンドを活用します。

### [GitHub Copilot アプリ][app]

複数のエージェントセッションを並行して実行し、セッションモードを切り替え、キャンバスで共同作業を行い、デスクトップアプリで GitHub issue とプルリクエストを管理します。

### [GitHub Copilot クラウドエージェント][cloud]

GitHub issue を非同期エージェントに割り当て、その作業を導き、進捗を監視し、エージェントが作成したプルリクエストをレビューします。

### [Visual Studio Code][vscode]

Visual Studio Code と GitHub Codespaces で GitHub Copilot を使用します。エディターを離れずに、Copilot Chat のエージェントモード、MCP サーバー、カスタムエージェントを活用します。

[cli]: cli/
[app]: app/
[cloud]: cloud/
[vscode]: vscode/
