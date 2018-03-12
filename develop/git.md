# Git

https://git-scm.com/
[公式ドキュメント](https://git-scm.com/book/ja/v2)

## ポイント

- 作業はこまめにコミットしましょう。
- コミットメッセージは作業内容が端的に一目で分かるようにしましょう。
- 作業単位でbranchを切りましょう。

## ブランチモデル

Git Flowがメジャーですが、毎日DeployするようなハイサイクルなプロジェクトではGitHub Flowが推奨されます。

### Git Flow

ローサイクルなプロジェクト向け。メジャーだが複雑。

https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html
https://github.com/nvie/gitflow

### GitHub Flow

ハイサイクルなプロジェクト向け。マイナーだがシンプル。

https://gist.github.com/Gab-km/3705015

- master = 公開できる状態として保守
- 作業単位でブランチを作成し、Pull Request を通して master を更新