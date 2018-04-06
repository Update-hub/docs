---
description: ソース管理ツール
---

# Git

## 公式サイト

{% embed data="{\"url\":\"https://git-scm.com/\",\"type\":\"link\",\"title\":\"Git\",\"icon\":{\"type\":\"icon\",\"url\":\"https://git-scm.com/favicon.ico\",\"aspectRatio\":0}}" %}

{% embed data="{\"url\":\"https://git-scm.com/book/ja/v2\",\"type\":\"link\",\"title\":\"Git - Book\",\"icon\":{\"type\":\"icon\",\"url\":\"https://git-scm.com/favicon.ico\",\"aspectRatio\":0},\"caption\":\"ドキュメント\"}" %}

### リポジトリサービス

* [GitHub](https://github.com) - 世界的メインストリーム。プライベートリポジトリは有料。
* [GitLab](https://about.gitlab.com/) - 国内の現場で採用率高。プライベートリポジトリも無料。
* [BitBucket](https://bitbucket.org/product) - プライベートリポジトリも無料（制限あり）

## TIps

#### Git管理のポイント

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

### クライアント

長期的にはコマンドでのGit操作が推奨されますが、コマンド操作が難しい方はクライアントの利用を検討してください。

* [GitHub Desktop](https://desktop.github.com/)
* [SourceTree](https://ja.atlassian.com/software/sourcetree)
* [https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる](https://get.slack.help/hc/ja/articles/232289568-GitHub-と-Slack-を連携させる)
* 通知の種類を増やす方法は[こちら](https://github.com/integrations/slack#configuration)



