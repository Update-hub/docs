# GitHub

## 作業手順

作業リポジトリをcloneします

```bash
git clone <リポジトリURL>
```

作業ディレクトリに移動します

```bash
cd <ディレクトリ>
```

作業ブランチを作成し、切り替えます

```bash
git checkout -b `feature/<作業内容>(英字)`
```

作業をコミットします

```bash
git commit -am '<作業内容>' #<issue番号>
```

e.g.

```bash
git commit -am リンク間違い修正 #23
```

作業をpushします

```bash
git push
```

* 英文でメッセージが出た場合（~ upstream ~ のような\)、そのメッセージをコマンドで入力し、実行してください

6.GitHUb上でPull Requestを出します

* Pull Requestの本文にissue番号を \# で記入してください。\(`#26`\)
* Pull Requestの作業内容を分かりやすく記載し、必要に応じてスクリーンショットを添付してください。

レビューで指摘が入ったら同じブランチで作業し、再度Pushしてください

すべての指摘に対応し、マージされたら作業完了です。

### レビュワー設定

下記の状態を使い分けで、コードに対してレビューを行ってください。

* Comment: 軽微な指摘、コメント
* Approve: 承認
* Request Change: 修正依頼

すべて対応されたのを確認したらマージし、マージ時に表示されるボタンからDelete Branchでブランチを削除します。さらに、紐づくissueを適宜closeしてください。

## Tips

### SlackとGitHub連携

SlackとGitHub連携を行うことでGitHubのアクティビティをSlackのチャンネルで知ることができます。チーム開発においてほぼ必須の連携です。

SlackとGitHubを連携させる（Updateはすでに連携済みなので不要です）

{% embed url="https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる" %}

関連チャンネルで下記のコマンドを打つ

```
/github subscribe <リポジトリURL or リポジトリパス> reviews comments branches
```

### GitHub Pagesで公開する

gh-pagesをグローバルにインストール

```bash
npm install -g gh-pages
```

プロジェクトディレクトリに移動し、公開コマンドを叩く

```bash
gh-pages -d <Deploy Directory>
```

GitHubのリポジトリページでGitHub Pagesを有効にし、対象ブランチを `gh-pages`ブランチにする。しばらく待つか、設定後に再度何かしらのdeployを行うことで見れるようになります。

![](../../.gitbook/assets/github-pages.png)

{% hint style="warning" %}
GitHub Pagesで公開されるページは第二階層目になるため、リンク先、ソース指定をルート相対（/hoge\)ではじめていたらリンク切れとなります。GitHub Pagesで公開する場合は必ず相対パス\(./hoge\)指定を行いましょう。
{% endhint %}
