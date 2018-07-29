# GitHub

## 作業手順

1.作業リポジトリをcloneします

```bash
$ git clone <リポジトリURL>
```

2.作業ディレクトリに移動します

```bash
$ cd <ディレクトリ>
```

3.作業ブランチを作成し、切り替えます

```bash
$ git checkout -b `feature/<作業内容>(英字)`
```

4.作業をコミットします

```bash
$ git commit -am '<作業内容>' #<issue番号>
```

e.g.

```bash
$ git commit -am リンク間違い修正 #23
```

5.作業をpushします

```bash
$ git push
```

* 英文でメッセージが出た場合（~ upstream ~ のような\)、そのメッセージをコマンドで入力し、実行してください

6.GitHUb上でPull Requestを出します

* Pull Request の本文にissue番号を \# で記入してください。\(`#26`\)
* Pull Request の作業内容を分かりやすく記載し、必要に応じてスクリーンショットを添付してください。

7.レビューで指摘が入ったら同じブランチで作業し、再度Pushしてください

8.すべての指摘に対応し、マージされたら作業完了です。

### レビュワー設定

下記の状態を使い分けで、コードに対してレビューを行ってください。

* Comment: 軽微な指摘、コメント
* Approve: 承認
* Request Change: 修正依頼

すべて対応されたのを確認したらマージし、マージ時に表示されるボタンから Delete Branch でブランチを削除します。さらに、紐づくissueを適宜closeしてください。

## Tips

### SlackとGitHub連携

SlackとGitHub連携を行うことでGitHubのアクティビティをSlackのチャンネルで知ることができます。チーム開発においてほぼ必須の連携です。

SlackとGitHubを連携させる（Updateは既に連携済みなので不要です）

{% embed data="{\"url\":\"https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる\",\"type\":\"link\",\"title\":\"GitHub と Slack を連携させる\",\"description\":\"GitHub は、ソフトウェア開発者のチームが共同でコードを記述し、プロジェクトを管理するためのツールです。GitHub を Slack に連携させれば、選択した Slack チャンネルであらゆるイベントの通知を受信できるようになります。一番よく使う重要度の高い2つのツールを連携させて、業務の状況を Slack 内から完全に把握できるようにしましょう。🛠  用途に合わせてアプリを選択   S...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://p4.zdassets.com/hc/settings\_assets/138842/200037786/vM8rHxxVKCakJZaTPOZ81Q-favicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://p4.zdassets.com/hc/settings\_assets/138842/200037786/yhcUITDtg0nMfANzyrWvIA-help-center-unfurl-image.png\",\"width\":192,\"height\":192,\"aspectRatio\":1}}" %}

関連チャンネルで下記のコマンドを打つ

```
/github subscribe <リポジトリURL or リポジトリパス> reviews comments branches
```

### GitHub Pages で公開する

gh-pages をグローバルにインストール

```bash
$ npm install -g gh-pages
```

プロジェクトディレクトリに移動し、公開コマンドを叩く

```bash
$ gh-pages -d <Deploy Directory>
```

GitHubのリポジトリページでGitHub Pagesを有効にし、対象ブランチを `gh-pages` ブランチにする。しばらく待つか、設定後に再度何かしらの deploy を行うことで見れるようになります。

![](../../.gitbook/assets/github-pages.png)

{% hint style="warning" %}
GitHub Pages で公開されるページは第二階層目になるため、リンク先、ソース指定をルート相対（/hoge\)ではじめていたらリンク切れとなります。GitHub Pages で公開する場合は必ず相対パス\(./hoge\)指定を行いましょう。
{% endhint %}

