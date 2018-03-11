# Git

https://git-scm.com/
[公式ドキュメント](https://git-scm.com/book/ja/v2)

## Git Flow

https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html
https://github.com/nvie/gitflow

## コミットメッセージ

コミットのタイトル、本文は自分以外の人が見たときに、どんな作業をしたのか？が一目で分かるようにしましょう。「作業」だけだと何をしたコミットなのかが分からないためプロジェクトによってコミットコメントがルール化されています。一例として Google の Angular プロジェクトのコメントルールをご紹介します。

作業タイプ(type)、 作業範囲(scrope) タイトル、 関連するissue番号（ある場合）を盛り込んだ下記フォーマットとなります。typeはあらかじめ決まっているので、適したtypeを設定してください。

```
<type>(<scope>): <subject> #issue
```

例: トップページにバナー追加した場合
```
feat(top): バナー追加 #23
```
#### Type一覧

|type|description|
|---|---|
|feat|新しい作業をするとき|
|fix|バグ修正、問題解決|
|docs|READMEなどドキュメント関連|
|style|インデント整えたりスペース入れたりと、コードの整形関連|
|refactor|無駄な記述をスマートにしたりと、正しいコーディングに整える作業|
|perf|コードチューニングをし、処理パフォーマンスを改善する場合|
|test|テスト関連|
|chore|開発環境やCIなどコアなファイル群に関する作業|