---
title: "演習 0: 前提条件"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

Copilot クラウドエージェントの演習を始める前に、必要な環境を準備します。Tailspin Toys リポジトリのコピーを作成し、指示ファイルの編集やクラウドエージェントの成果のレビューに使う [Codespace][codespaces] を起動します。

## 演習用リポジトリをセットアップする

コードの作業に使うリポジトリのコピーを作成するため、[テンプレート][template-repository]から新しいリポジトリを作成します。新しいリポジトリには演習に必要なファイルがすべて含まれます。

1. 新しいブラウザー ウィンドウで、[Tailspin Toys テンプレート][tailspin-template]を開きます。
2. 演習用リポジトリのページで **Use this template** を選択し、リポジトリのコピーを作成します。次に **Create a new repository** を選択します。

    ![Use this template ボタン](../../../_images/ex0-use-template.png)

3. GitHub または Microsoft が主催するイベントでワークショップに参加している場合は、メンターの指示に従います。それ以外の場合は、GitHub Copilot を利用できる組織に新しいリポジトリを作成します。

    ![テンプレート リポジトリの設定](../../../_images/ex0-repository-settings.png)

4. 作成したリポジトリのパス (**organization-or-user-name/repository-name**) をメモします。後の演習で使用します。

## Codespace を作成する

次に、Codespace を使って演習を進めます。

[GitHub Codespaces][codespaces] は、ブラウザー上で直接コードの記述、実行、デバッグができるクラウド開発環境です。複数のプログラミング言語、拡張機能、ツールに対応した IDE を利用できます。

1. 作成したリポジトリを開きます。
2. 緑色の **Code** ボタンを選択します。

    ![Code ボタンを選択](../../../_images/ex0-code-button.png)

3. **Codespaces** タブを選択し、**+** ボタンを選択して Codespace を作成します。

    ![Codespace を作成](../../../_images/ex0-create-codespace.png)

Codespace の作成には数分かかりますが、必要なサービスを手動でインストールするよりもずっと早く準備できます。その間に GitHub Copilot のほかの機能を確認してみましょう。

> [!CAUTION]
> 今後の演習でこの Codespace に戻ります。ひとまずブラウザーのタブを閉じずに残しておいてください。

> [!NOTE]
> このワークショップは Codespace またはローカルの[開発コンテナー][dev-containers]で実行できます。どちらの環境にも、演習に必要な前提条件が用意されています。ローカルで実行する場合は、クローンしたリポジトリを VS Code で開き、表示されたら **Reopen in Container** を選択します。VS Code が Codespace と同じ開発コンテナーを構築します。

[codespaces]: https://github.com/features/codespaces
[dev-containers]: https://code.visualstudio.com/docs/devcontainers/containers

## まとめ

演習用リポジトリのコピーを作成し、Copilot クラウドエージェントと作業するための Codespace の作成を開始しました。

## 次のステップ

クラウドエージェントが従うカスタム指示を追加します。[演習 1: カスタム指示][next-lesson]に進みます。

## リソース

- [GitHub Codespaces の概要][codespaces]
- [テンプレートからリポジトリを作成する][template-repository]
- [Codespaces の使用を開始する][codespaces-quickstart]

[tailspin-template]: https://github.com/github-samples/tailspin-toys
[template-repository]: https://docs.github.com/repositories/creating-and-managing-repositories/creating-a-template-repository
[codespaces-quickstart]: https://docs.github.com/codespaces/getting-started/quickstart
[next-lesson]: ../1-custom-instructions/
