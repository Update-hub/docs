# git

* [公式サイト](https://git-scm.com/)
* [公式ドキュメント](https://git-scm.com/book/ja/v2)

## リポジトリサービス

* [GitHub](https://github.com) - 世界的メインストリーム。プライベートリポジトリは有料。
* [GitLab](https://about.gitlab.com/) - 国内の現場で採用率高。プライベートリポジトリも無料。
* [BitBucket](https://bitbucket.org/product) - プライベートリポジトリも無料（制限あり）

## Git管理のポイント

* 作業はこまめにコミットしましょう。
* コミットメッセージは作業内容が端的に一目で分かるようにしましょう。
* issueに紐づく作業の場合はコメントの後ろに `作業内容 #4` などとissue番号を追記しましょう。
* 作業単位\(issue単位\)でbranchを切りましょう。

## ブランチモデル

Git Flowがメジャーですが、毎日DeployするようなハイサイクルなプロジェクトではGitHub Flowが推奨されます。

### GitHub Flow

ハイサイクルなプロジェクト向け。マイナーだがシンプル。

[https://gist.github.com/Gab-km/3705015](https://gist.github.com/Gab-km/3705015)

* master = 公開できる状態として保守
* 作業単位でブランチを作成し、Pull Request を通して master を更新

### Git Flow

ローサイクルなプロジェクト向け。メジャーだが複雑。

[https://danielkummer.github.io/git-flow-cheatsheet/index.ja\_JP.html](https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html) [https://github.com/nvie/gitflow](https://github.com/nvie/gitflow)

## クライアント

長期的にはコマンドでのGit操作が推奨されますが、コマンド操作が難しい方はクライアントの利用を検討してください。

* [GitHub Desktop](https://desktop.github.com/)
* [SourceTree](https://ja.atlassian.com/software/sourcetree)
* [https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる](https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる)
* 通知の種類を増やす方法は[こちら](https://github.com/integrations/slack#configuration)

## その他

* github プロジェクトの場合、基本的にgithubのコメントベースで情報交換するのが吉です。途中でメンバーの入れ替わりがあった時に、後任者がおいやすいため。（チャット空間など色々なところで分散していると情報が追いづらい）
