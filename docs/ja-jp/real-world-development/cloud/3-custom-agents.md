---
title: "演習 3: カスタム エージェント"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

## カスタム エージェントとは

GitHub Copilot の[カスタム エージェント][custom-agents-concept]を使うと、開発ワークフロー内の特定のタスクや分野に合わせた AI アシスタントを作成できます。リポジトリの `.github/agents` フォルダーに Markdown ファイルを作成してエージェントを定義し、対象を絞った指示、ベスト プラクティス、コーディング パターン、ドメイン固有の知識を Copilot に提供できます。チームの専門知識を再利用可能なエージェントとしてまとめることもできます。たとえば、[WCAG][wcag] 準拠を確認するアクセシビリティ エージェント、安全なコーディングを支援するセキュリティ エージェント、一貫したテスト パターンを維持するテスト エージェントです。

カスタム エージェントは、プロジェクトの `.github/agents` フォルダー内の Markdown ファイル、またはグローバルな `~/.copilot/agents` に定義します。各ファイルには、少なくとも `name` と `description` を含む YAML frontmatter を記述し、その後にエージェントの動作、専門知識、指示を定義する Markdown プロンプトを記述します。

### カスタム エージェントとエージェント スキルの違い

カスタム エージェントと[エージェント スキル][agent-skills-concept]には一部共通点があります。どちらも主に Markdown ファイルで定義され、AI に作業方法を伝えます。最も分かりやすい違いは、**カスタム エージェントが作業者**で、**スキルがツール**であることです。

カスタム エージェントには独自のコンテキスト ウィンドウがあり、作業の一環としてスキルやほかのエージェントをまとめて調整できます。この演習では、アクセシビリティ カスタム エージェントがアクセシビリティ ガイドラインに沿ってサイトをレビュー、更新します。その際、プルリクエストのワークフローやテストの実行と管理を行うスキルを呼び出すこともできます。

> [!NOTE]
> カスタム エージェントの作成に唯一の正解はありません。ほかの AI 機能と同様に、環境やシナリオに合う方法を見つけるまで試して調整してください。

[custom-agents-concept]: https://docs.github.com/copilot/concepts/agents/cloud-agent/about-custom-agents
[agent-skills-concept]: https://docs.github.com/copilot/concepts/agents/about-agent-skills
[wcag]: https://www.w3.org/WAI/standards-guidelines/wcag/

この演習では、次の操作を行います。

- カスタム エージェントの定義方法を確認します。
- カスタム エージェントにタスクを割り当てます。

## シナリオ

Tailspin Toys は、視覚能力や好みにかかわらず、すべての人がクラウドファンディング プラットフォームを利用できるように取り組んでいます。最近、現在のダーク テーマは文字と背景のコントラストが不十分で、読みにくいというフィードバックがありました。このアクセシビリティの課題に対応するため、デザイン チームは切り替え可能なハイ コントラスト モードを求めています。

アクセシビリティは重要なため、できるだけ早く実装します。機能の生成にはカスタム エージェントを使用します。

## アクセシビリティ カスタム エージェントを確認する

アクセシビリティ用のカスタム エージェントは作成済みです。Copilot をどのように導くか理解するため、内容を確認しましょう。

Codespace に戻り、アクセシビリティ カスタム エージェントのファイルを確認します。

1. `.github/agents/accessibility.md` を開きます。
2. YAML frontmatter の `name` と `description` フィールドを確認します。

> [!CAUTION]
> カスタム エージェントには `name` と `description` を含む frontmatter が必要です。

3. 続くセクションを確認します。次の内容が記載されています。
   - アクセシブルな Web サイトのコード生成における主な責任。
   - アクセシビリティのベスト プラクティス。
   - HTML、CSS、JavaScript のコード例。
   - よくある問題や間違い。

## issue を作成して割り当てる

ミッション コントロールは、環境内のエージェントを操作する場所です。Copilot クラウドエージェントにタスクを割り当てたり、進行状況を監視したり、追加の指示を与えたりできます。ハイ コントラスト モードの作成を Copilot に割り当てましょう。

1. リポジトリに移動します。
2. **Issues** タブを選択します。
3. **New issue** を選択して、新しい issue のダイアログを開きます。
4. **Blank issue** を選択して issue を作成します。
5. **Title** に `Add high contrast mode to website` と入力します。
6. **Description** に次を入力します。

    ```plaintext
    We need a high contrast mode for the site. There should be a toggle for high contrast which the user can set. It should store the setting in local storage on the browser.
    ```

7. **Create** を選択して issue を作成します。
8. 右側の **Assign to Copilot** を選択して、割り当てダイアログを開きます。
9. カスタム エージェントの一覧から **Accessibility agent** を選択します。

    ![クラウドエージェントの割り当て画面。Accessibility カスタム エージェントが強調表示されています](../../../_images/ex5-select-custom-agent.png)

10. **Assign** を選択します。
11. Copilot がバックグラウンドで作業を開始します。

## まとめと次のステップ

このレッスンでは、特定のタスクや分野に合わせた AI アシスタントである [GitHub Copilot のカスタム エージェント][custom-agents]について学びました。カスタム エージェントを使うと、チームの専門知識と標準を再利用可能なエージェントにまとめ、Copilot の作業をより効果的に導くことができます。

次の概念を確認しました。

- カスタム エージェントの定義方法。
- カスタム エージェントへのタスクの割り当て方。

Copilot がハイ コントラスト モードを実装している間に、ミッション コントロールから[エージェント セッションを監視して方向付け][next-lesson]ます。

## リソース

- [カスタム エージェントについて][custom-agents]
- [組織でカスタム エージェントを利用する準備][org-custom-agents]
- [エンタープライズでカスタム エージェントを利用する準備][enterprise-custom-agents]

---

| [← 前のレッスン: GitHub Copilot クラウドエージェント][previous-lesson] | [次のレッスン: エージェントの監視と管理 →][next-lesson] |
|:--|--:|

[previous-lesson]: ../2-cloud-agent/
[next-lesson]: ../4-managing-agents/
[custom-agents]: https://docs.github.com/copilot/concepts/agents/cloud-agent/about-custom-agents
[org-custom-agents]: https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-organization/prepare-for-custom-agents
[enterprise-custom-agents]: https://docs.github.com/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-agents/prepare-for-custom-agents
