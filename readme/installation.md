---
description: まずは実務に必要な環境を整えてください。
---

# 事前準備

## 概要

まずは実務に必要な環境を用意してください。

## PC

Mac or Windows を用意してください。実際の現場ではMacが多いため、これからPCを購入する方はMacをお勧めします。また、各種サービスにログインするので共用PCは使わないでください。基本的に使わないようにしてください。

* Macであればスペックは不問です。Mac Book Pro の Touch Bar なしのどれかをオススメします。
* Macの場合**英字キーボード**（Apple Store Onlineから購入可能）がお勧めです。
* Windows の場合、基本的なPC操作でもたつかない程度の処理能力が推奨されます。

## ツール

以下のツールをそれぞれインストールしてください。すべて無料です。

* [Visual Studio Code](https://code.visualstudio.com/Download) - エディタ
* [git](https://git-scm.com/) - コード管理ツール
* [node](https://nodejs.org/ja/download/) - JS実行環境
* [chrome](https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&amp;hl=ja) - 主な開発用ブラウザ
* [slack](https://slack.com/downloads/) - チャットツール（スマホアプリも同様）
* [Adobe Creative Cloud](https://www.adobe.com/jp/creativecloud/desktop-app.html) - Adobe製品
* [SourceTree](https://ja.atlassian.com/software/sourcetree) - Git管理ツール

slackをインストールしたら[Update](https://update-hub.slack.com)のワークスペースにログインしてください。Slackはスマートフォンアプリもあるのでこちらもインストールしてください。**稼働中はSlackアプリにログインする**ようにしてください。

### node package

windowsの場合コマンドプロンプト、macの場合ターミナルで下記コマンドを打つ

{% hint style="info" %}
コードビューで $ が先頭にある場合、黒い画面（ターミナル、コマンドプロンプト）での操作を意味します。また、コードを貼り付ける際は $ は不要ですのでコピーに含めないよう、注意しましょう。
{% endhint %}

```bash
$ npm i -g gulp-cli eslint editorconfig
```

### Visual Studio Code拡張機能

* [Editor Config](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) - コーディングルール定義
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - JSの品質チェック
* [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify) - コード整形

## その他の設定

### GitLab登録

[GitLab](https://gitlab.com/)アカウント作成後、アイコンを設定してください。その後、GitLabの設定を行ってください。

{% page-ref page="../documents/base/gitlab.md" %}

### Slackの設定

以下の設定を行ってください。

* プロフィールの表示名をGitHubのアカウント名 \(自分のGitHubページのURLの末尾\)と同じにしてください。
* プロフィール画像を設定してください。
* 新着メッセージを見落としがちな方は、環境設定 &gt; 通知のタイミングで、「すべての新規メッセージ」から通知が来るように変更してください。（任意）

