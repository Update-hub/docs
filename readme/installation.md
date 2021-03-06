---
description: まずは実務に必要な環境を整えてください。
---

# 事前準備

## 概要

まずは実務に必要な環境を用意してください。

## PC

Mac or Windowsを用意してください。実際の現場ではMacが多いため、これからPCを購入する方はMacをオススメします。また、各種サービスにログインするので共用PCは使わないでください。

* Macであればスペックは不問です。MacBook ProのTouch Barなしのどれかをオススメします。
* Macの場合**英字キーボード**（Apple Store Onlineから購入可能）がオススメです。
* Windowsの場合、基本的なPC操作でもたつかない程度の処理能力が推奨されます。

## ツール

以下のツールをそれぞれインストールしてください。すべて無料です。

* [Visual Studio Code](https://code.visualstudio.com/Download) - エディター
* [git](https://git-scm.com/) - コード管理ツール
* [node](https://nodejs.org/ja/download/) - JS実行環境
* [chrome](https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&amp;hl=ja) - 主な開発用ブラウザ
* [slack](https://slack.com/downloads/) - チャットツール（スマホアプリも同様）
* [Adobe Creative Cloud](https://www.adobe.com/jp/creativecloud/desktop-app.html) - Adobe製品
* [Adobe XD](https://www.adobe.com/jp/products/xd.html)

slackをインストールしたら[Update](https://update-hub.slack.com)のワークスペースにログインしてください。Slackはスマートフォンアプリもあるのでこちらもインストールしてください。**稼働中はSlackアプリにログイン**してください。

### node package

windowsの場合コマンドプロンプト、macの場合ターミナルで下記コマンドを打つ

```bash
npm i -g gulp-cli eslint editorconfig
```

`permisson denied`的なエラーがでた場合はコマンドの前に`sudo`をつけましょう。つまり以下のようになります。

```bash
sudo npm i -g gulp-cli eslint editorconfig
```

この際、`password:`のような表記が出たら、そのままPCのパスワードを入力してエンターしてください。（パスワードの入力中は文字が表示されないので注意してください）

### Visual Studio Code拡張機能

* [Editor Config](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) - コーディングルール定義
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - JSの品質チェック
* [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify) - コード整形
* [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja) - 日本語化

## その他の設定

### GitLab登録

* [GitLab](https://gitlab.com/)アカウント作成後、アイコンを設定してください。その後、GitLabの設定を行ってください。
* GitLabのプロフィール設定画面から言語を日本語にしてください。

{% page-ref page="../documents/base/gitlab.md" %}

### GitHub登録

{% embed url="https://github.com/Update-hub" %}

### Slackの設定

以下の設定を行ってください。

* プロフィールの表示名をGitLabのアカウント名 \(自分のGitLabページのURLの末尾\)と同じにしてください。
* プロフィール画像を設定してください。
* 新着メッセージを見落としがちな方は、環境設定 &gt; 通知のタイミングで、「すべての新規メッセージ」から通知が来るように変更してください。（任意）
