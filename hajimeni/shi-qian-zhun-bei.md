# 事前準備

## PC

Mac or Windows を用意してください。実際の現場ではMacが多いため、これからPCを購入する方はMacをお勧めします。

* Macであればスペックは不問です。
* Macの場合**英字キーボード**（Apple Store Onlineか購入可能）がお勧めです。
* Windows の場合、基本的なPC操作でもたつかない程度の処理能力が推奨されます。

## ツール

以下のツールをそれぞれインストールしてください。すべて無料です。

* [Visual Studio Code](https://code.visualstudio.com/Download) - エディタ
* [git](https://git-scm.com/) - コード管理ツール
* [node](https://nodejs.org/ja/download/) - JS実行環境
* [chrome](https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&amp;hl=ja) - 主な開発用ブラウザ
* [slack](https://slack.com/downloads/) - チャットツール
* [yarn](https://yarnpkg.com/lang/ja/docs/install/) - node パッケージ管理ツール

slackをインストールしたらUpdateのワークスペース\(update-hub.slack.com\)にログインしてください。Slackはスマートフォンアプリもあるのでこちらもインストールをお勧めします。Web版ではなくアプリを使い、**作業中は基本的にSlackにログインする**ようにしてください。

### node package

windowsの場合コマンドプロンプト、macの場合ターミナルで下記コマンドを打つ

{% hint style="info" %}
コードビューで $ が先頭にある場合、黒い画面（ターミナル、コマンドプロンプト）での操作を意味します。また、コードを貼り付ける際は $ は不要ですのでコピーに含めないよう、注意しましょう。
{% endhint %}

```bash
$ npm i -g gulp-cli
$ npm i -g eslint
$ npm i -g editorconfig
```

### Visual Studio Code拡張機能

* [Editor Config](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) - コーディングルール定義
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - JSの品質チェック
* [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify) - コード整形

## その他の設定

### GitHub登録

* [GitHub](https://github.com/)

アカウント作成後、アイコンの設定を行ってください。また、作成したメールアドレスとユーザー名を下記コマンドでgitに定義してください。コマンドはターミナル\(mac）かgit bash\(windows\)で行ってください。

```bash
$ git config --global user.name ユーザー名
$ git config --global user.email メールアドレス
```

### Slackの設定

以下の設定を行ってください。

* プロフィールの表示名をGitHubのアカウント名 \(自分のGitHubページのURLの末尾\)と同じにしてください。
* プロフィール画像を設定してください。
* 環境設定 &gt; 通知のタイミングで、「すべての新規メッセージ」から通知が来るように変更してください。

{% hint style="info" %}
すべての準備が終わったら Slack で @deerboy に連絡してください。
{% endhint %}

