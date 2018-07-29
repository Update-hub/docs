---
description: Gitはソースコードの管理に欠かせない必須ツールです。
---

# Git

## 概要

Gitを使えば、ソースコードのバージョン管理を行ったり、複数人で共通のコードをメンテナンスすることができます。ほぼすべての制作現場で使われているので、基本的な使い方をマスターしましょう。コマンド操作は通常GUIで操作することが多いので、GUIで解説を行います。

{% embed data="{\"url\":\"https://git-scm.com/\",\"type\":\"link\",\"title\":\"Git\",\"icon\":{\"type\":\"icon\",\"url\":\"https://git-scm.com/favicon.ico\",\"aspectRatio\":0}}" %}

{% embed data="{\"url\":\"https://git-scm.com/book/ja/v2\",\"type\":\"link\",\"title\":\"Git - Book\",\"icon\":{\"type\":\"icon\",\"url\":\"https://git-scm.com/favicon.ico\",\"aspectRatio\":0},\"caption\":\"ドキュメント\"}" %}

### 代表的なGUI

* [GitHub for Desktop](https://desktop.github.com/) - GitHubリポジトリに特化
* [Sourcetree](https://ja.atlassian.com/software/sourcetree) - 汎用性が高く、メジャー
* [Visual Studio Code ](https://code.visualstudio.com/)- Git管理機能を内臓
* その他エディター内臓の機能

### 代表的なリポジトリサービス

* [GitLab](https://about.gitlab.com/) - 実務での採用率が高い。プライベートリポジトリも無料。
* [GitHub](https://github.com) - OSSで人気。プライベートリポジトリは有料。
* [BitBucket](https://bitbucket.org/product) - プライベートリポジトリも無料（制限あり）

## クイックスタート

### 基本的な流れ

既存のGitプロジェクトを自分のPCに複製する

```bash
$ git clone http://.....
```

ブランチを作成する\(new-branch という名前のブランチを作成する例）

```bash
$ git branch new-branch
```

 ブランチを切り替える

```bash
$ git checkout new-branch
```

作業内容をコミットする

```bash
$ git add .
$ git commit -m '<コミットメッセージ>'
```

issueに紐づく作業の場合、コミットメッセージの最後にissue番号を記載しましょう

```bash
$ git commit -m 'リンク先を修正 #23' // #23 のissueに紐づく作業の場合
```

作業内容をPushする

```bash
$ git push
```

他の人の作業を取り込む

```bash
$ git pull
```

## リファレンス

### 特定のコミットを取り消したい

```bash
$ git log // 作業ログの確認（取り消したいコミットのコミットIDを控える）
$ git revert <コミットID> // コミットメッセージを聞かれるので適宜編集して保存
```

### 直前のコミットに現状の作業を追加したい

{% hint style="warning" %}
amendを行った場合 Force Push（強制Push）が必要になります。
{% endhint %}

```bash
$ git commit -a --amend // コミットメッセージを聞かれるので適宜編集して保存
```

### 現在の作業内容を確認したい

```bash
$ git diff
```

### 現在の編集されているファイル群を確認したい

```bash
$ git status
```

### コミット間の差分をzipでまとめたい

クライアントに作業内容を提出する際に便利です。

```text
git archive master --format=zip -o diff.zip --prefix=data/ `git diff --name-only --diff-filter=d コミットA コミットB`
```

## Gitクライアント

Gitクライアントを使うとコマンドを使わなくても直感的にGitの基本操作を行うことができます。

* [Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol)
* [GitHub for Desktop](https://desktop.github.com/)
* [SourceTree](https://www.sourcetreeapp.com/)

## Tips

### Git管理のポイント

* 作業はこまめにコミットしましょう。
* コミットメッセージは作業内容が端的に一目で分かるようにしましょう。
* issueに紐づく作業の場合はコメントの後ろに `作業内容 #4` などとissue番号を追記しましょう。
* 作業単位\(issue単位\)でbranchを切りましょう。

### ブランチモデル

Git Flowがメジャーですが、毎日DeployするようなハイサイクルなプロジェクトではGitHub Flowが推奨されます。

#### GitHub Flow

[https://gist.github.com/Gab-km/3705015](https://gist.github.com/Gab-km/3705015)

ハイサイクルなプロジェクト向け。マイナーだがシンプル

* master = 公開できる状態として保守
* 作業単位でブランチを作成し、Pull Request を通して master を更新

#### Git Flow

ローサイクルなプロジェクト向け。メジャーだが複雑。

[https://danielkummer.github.io/git-flow-cheatsheet/index.ja\_JP.html](https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html) [https://github.com/nvie/gitflow](https://github.com/nvie/gitflow)

### マージ時にコンフリクトした場合

プルリクエストをマージする際にコンフリクトが発生した場合は、以下のようにして対応します。（決してmasterブランチを直接いじろうとしないこと）

1. PR対象のブランチ\(最新の状態\)を作業ブランチに取り込む\(merge XXX\)
2.  コンフリクトを解消する
3.  作業ブランチを再度Pushする
4.  コンフリクトが消えており、PRが通る状態になっている

1.の時点でコンフリクトが出ているはずなので、エディターでプロジェクト内を &gt;&gt;&gt; で一括検索すると競合箇所が分かります。Visual Studio Codeには競合の解決機能がついているので、それでmasterか自分のブランチか正しい方（あるいは両方）を取り込み、コンフリクトを解消してから3.に進みます。
