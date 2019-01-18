---
description: 最もよく使われるリポジトリ管理サービス
---

# GitLab

## 概要

{% embed url="https://www.youtube.com/playlist?list=PLw1QAmLkyyahd9SWHMmo-agcrsSDRYQSQ" %}

GitLabは業務においてもっともよく使われるリポジトリ管理サービスです。GitHubは不特定多数でのオープンソース開発に適していますが、GitLabは会社やチームでのクローズドな開発で使われます。GitHubと違い、無料でプライベートリポジトリを作成できます。

## 事前準備

1. ユーザー登録を行いましょう。
2. [ローカルのGit設定](gitlab.md#rkarunogit)を行いましょう。
3. [2段階認証](gitlab.md#2-duan)を設定しましょう。

### 2段階認証

{% hint style="danger" %}
この設定は個人のPC（スマホ）に依存するため、共有端末では行わないようにしてください。
{% endhint %}

2段階認証をすることで、第三者の不正ログインを防ぎます。クライアントの機密コードを取り扱う都合、必ず2段階認証を行いましょう。

1. [設定 &gt; Account](https://gitlab.com/profile/account) &gt; **Two-Factor Authentication** を有効にする
2. 設定 &gt; SSH Keysで、SSH Keyを登録する\([SSH Key の作り方](https://gitlab.com/help/ssh/README#generating-a-new-ssh-key-pair)、[過去作ったKeyの取得](https://gitlab.com/help/ssh/README#locating-an-existing-ssh-key-pair)）

設定時、[認証アプリ](https://itunes.apple.com/jp/app/google-authenticator/id388497605?mt=8)が必要になります。事前にダウンロードしましょう。以後、新しい環境からログインを試みると2段階認証が必要になるので、認証アプリで表示される認証コードを利用してログインしましょう。

なお、2段階認証を使うことでGitのCloneに使用するURLが `http://`  から `git@` に変わります。httpプロトコルのリポジトリURLは以後使用できなくなるため、既存のリポジトリがある場合はgit@~ のURLに変更しましょう。

### ローカルのGit設定

GitLabに登録したメールアドレスとユーザー名をローカルのGitに紐付けましょう。以下のコマンドをターミナルで叩いてください。名前とメールアドレスは自分のものに変えてください。間違えて設定してしまった場合は、再度コマンドを叩いて設定し直してください。

```bash
git config --global user.name "Taro Yamada"
git config --global user.email "taro.yamada@deer.co.jp"
```

なお、基本的にこの設定はGitHubなど他のリポジトリサービスにも影響するため、各サービスでユーザー名やメールアドレスを統一しておきましょう。

## Tips

### 主なフロー

1. プロジェクト（リポジトリ）を作成しましょう。
2. リポジトリをCloneしましょう。
3. issue（課題）ごとにブランチを作成（feature/issue番号）します。
4. 作業が終わったらmasterにマージリクエストを出します。
5. マージされたらissueをクローズします。

### 作業中のMRにはWIPをつける

WIPをつけることでマージできなくなります。マージリクエストのレビューに対し修正を行っている時などはWIPをつけましょう。

### 公開する

`gitlab-cli.yml`を設置します。開発環境によって異なりますが、ビルドを必要としないサイトの場合、リポジトリのCI設定画面よりHTMLのテンプレートを選ぶことで、masterにpushした際、publicディレクトリの内容が公開されるようになります。（自分がオーナーのリポジトリでのみ可能）

### Merge Requestの並立

作業内容がバッティングしない場合、Merge Requestのレビューを待っている間に他のIssueを進め、新たなMerge Requestを出すことが可能です。

### ポイント

* masterはマージリクエスト、ソースレビューを通過したものが反映されるので、masterブランチを直接編集しないようにします。
* 作業ブランチにまつわるコミットは、コミットメッセージの後ろにissue番号を付与します。（issue番号24のブランチで画像修正を行う場合）

```text
画像修正 #24
```
