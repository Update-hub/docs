---
description: 最もよく使われるリポジトリ管理サービス
---

# GitLab

## 概要

GitLabは業務において最もよく使われるリポジトリ管理サービスです。GitHubは不特定多数でのオープンソース開発に適していますが、GitLab は会社やチームでのクローズドな開発で使われます。GitHub と違い、無料でプライベートリポジトリを作成することができます。

## 事前準備

1. ユーザー登録を行いましょう。
2. [ローカルのGit設定](gitlab.md#rkarunogit)を行いましょう。
3. [2段階認証](gitlab.md#2-duan)を設定しましょう。

### 2段階認証

2段階認証をすることで、第三者の不正ログインを防ぎます。クライアントの機密コードを取り扱う都合、必ず２段階認証を行いましょう。

1. [設定 &gt; Account](https://gitlab.com/profile/account) &gt; **Two-Factor Authentication** を有効にする
2. 設定 &gt; SSH Keys で、SSH Key を登録する\([SSH Key の作り方](https://gitlab.com/help/ssh/README#generating-a-new-ssh-key-pair)、[過去作ったKeyの取得](https://gitlab.com/help/ssh/README#locating-an-existing-ssh-key-pair)）

設定時、[認証アプリ](https://itunes.apple.com/jp/app/google-authenticator/id388497605?mt=8)が必要になります。事前にダウンロードしましょう。以後、新しい環境からログインを試みると２段階認証が必要になるので、認証アプリで表示される認証コードを利用してログインしましょう。

なお、２段階認証を使うことでGitのCloneに使用するURLが `http://`  から `git@` に変わる点に注意しましょう。httpプロトコルのリポジトリURLは以後使用できなくなるため、既存のリポジトリがある場合はgit@~ のURLに変更しましょう。

### ローカルのGit設定

GitLab に登録したメールアドレスとユーザー名をローカルのGitに紐付けましょう。以下のコマンドをターミナルで叩いてください。名前とメールアドレスは自分のものに変えてください。間違えて設定してしまった場合は、再度コマンドを叩いて設定し直してください。

```text
$ git config --global user.name "Taro Yamada"
$ git config --global user.email "taro.yamada@deer.co.jp"
```

なお、基本的にこの設定はGitHubなど他のリポジトリサービスにも影響するため、各サービスでユーザー名やメールアドレスを統一しておきましょう。

## プロジェクトで使いこなす

1. プロジェクト（リポジトリ）を作成しましょう。
2. コマンドラインツールやSource Tree などを使ってリポジトリをClone しましょう。
3. 以後、通常通り開発を行います。

### 

