---
description: Gitはソースコードの管理に欠かせない必須ツールです。
---

# Git

## チュートリアル

{% embed url="https://www.youtube.com/playlist?list=PLw1QAmLkyyaiklAgOMsVzhh1kWD-mTO_c" caption="シリーズになっています" %}

### 競合の解説

{% embed url="https://youtu.be/pYkJ_34YoVA?t=1234" caption="" %}

## 概要

{% embed url="https://www.youtube.com/watch?v=sY64kVwQ-bw&index=3&t=278s&list=PLw1QAmLkyyagylcEKmXLzSA6XgaxV4ofL" %}

Gitを使えば、ソースコードのバージョン管理を行ったり、複数人で共通のコードをメンテナンスできます。ほぼすべての制作現場で使われているので、基本的な使い方をマスターしましょう。コマンド操作は通常GUIで操作することが多いので、GUIで解説を行います。

現場に入ったらクライアントやメンバーから「〜からブランチ切って〜にpushしといて〜」みたいなワードがナチュラルに飛び交います。なので、概念や操作を理解できてないと死にます。しっかり理解してください。

{% embed url="https://git-scm.com/" %}

{% embed url="https://git-scm.com/book/ja/v2" caption="ドキュメント" %}

### 代表的なGUI

* [Sourcetree](https://ja.atlassian.com/software/sourcetree) - 汎用性が高く、メジャー
* [Visual Studio Code](https://code.visualstudio.com/)- Git管理機能を内臓

### 代表的なリポジトリサービス

* [GitLab](https://about.gitlab.com/) - 実務での採用率が高い。プライベートリポジトリも無料。
* [GitHub](https://github.com) - OSSで人気。プライベートリポジトリは有料。
* [BitBucket](https://bitbucket.org/product) - プライベートリポジトリも無料（制限あり）

## クイックスタート

初心者の方はVS CodeなどのGUIでの操作を推奨します。GUIを使わない方は以下のコマンドを参照してください。

### 基本的な流れ

既存のGitプロジェクトを自分のPCに複製する

```bash
git clone http://.....
```

ブランチを作成する\(new-branchという名前のブランチを作成する例）

```bash
git branch new-branch
```

 ブランチを切り替える

```bash
git checkout new-branch
```

作業内容をコミットする

```bash
git add .
git commit -m '<コミットメッセージ>'
```

issueに紐づく作業の場合、コミットメッセージの最後にissue番号を記載しましょう

```bash
git commit -m 'リンク先を修正 #23' // #23 のissueに紐づく作業の場合
```

作業内容をPushする

```bash
git push
```

他の人の作業を取り込む

```bash
git pull
```

### ゼロからGit管理をはじめる場合

プロジェクトディレクトリで

```bash
git init
git add .
git remote add origin <リポジトリURL>
git push
```

## Git管理のポイント

各作業ブランチは必ず**masterから**作成します。ブランチは通常現在のブランチを元に作られます。（作成時に元となるブランチを指定する方法もありますが）たとえばAの作業を行ったブランチにいる状態でブランチBを作成すると、Aの作業を含んだブランチBが誕生します。Aにバグが潜んでいた場合、バグがブランチBにも引き継がれます。また、その状態でブランチBのマージリクエストを出すとコードの差分にAの作業も含まれるため、レビューにも支障をきたします。

* 作業はこまめにコミットしましょう。
* コミットメッセージは作業内容が端的に一目でわかるようにしましょう。
* issueに紐づく作業の場合はコメントの後ろに `作業内容 #4` などとissue番号を追記しましょう。
* 作業単位\(issue単位\)で**masterから**branchを切りましょう。

### GitHub Flow

masterから作業ブランチを作成し、終わったらマージリスクエストをだすもっともシンプルなブランチ管理手法です。

## Tips

### 特定のコミットを取り消したい

SourceTreeなどでは右クリックから簡単にコミットの打ち消しができます。

```bash
git log // 作業ログの確認（取り消したいコミットのコミットIDを控える）
git revert <コミットID> // コミットメッセージを聞かれるので適宜編集して保存
```

### 直前のコミットに現状の作業を追加したい

{% hint style="warning" %}
amendを行った場合Force Push（強制Push）が必要になります。
{% endhint %}

```bash
git commit -a --amend // コミットメッセージを聞かれるので適宜編集して保存
```

### 現在の作業内容を確認したい

```bash
git diff
```

### 現在の編集されているファイル群を確認したい

```bash
git status
```

### コミット間の差分をzipでまとめたい

クライアントに作業内容を提出する際に便利です。

```text
git archive master --format=zip -o diff.zip --prefix=data/ `git diff --name-only --diff-filter=d コミットA コミットB`
```

### マージ時にコンフリクトした場合

プルリクエストをマージする際にコンフリクトが発生した場合は、以下のようにして対応します。（決してmasterブランチを直接いじろうとしないこと）

1. PR対象のブランチ\(多くの場合最新のmaster\)をローカルの作業ブランチに取り込む\(merge XXX\)
2. コンフリクトを解消する（他の人や他のIssueの作業を間違えて消さないように注意）
3. 作業ブランチを再度Pushする（改めてPRを出し直す必要はない）
4. コンフリクトが消えており、PRが通る状態になっている

1の時点でコンフリクトが出ているはずなので、エディターでプロジェクト内を`<<<`で一括検索すると競合箇所が分かります。Visual Studio Codeには競合の解決機能がついているので、それでmasterか自分のブランチか正しい方（あるいは両方）を取り込み、コンフリクトを解消してから3に進みます。

### 作業内容を退避したい

ブランチで作業中、諸事情で他のブランチに切り替える必要がある場合、いったんコミットする人がいますが、中途半端な状態のコミットは避けるべきです。その場合は作業内容をstash（一時退避）できます。
