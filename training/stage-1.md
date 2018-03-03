# 1. 基礎トレーニング

共同開発をする上で必要な知識を身につけてください。

## カリキュラム

- [gitによる共同開発](https://www.youtube.com/watch?v=sY64kVwQ-bw&list=PLw1QAmLkyyagylcEKmXLzSA6XgaxV4ofL&index=2)

## 共同開発マナー

- コミットメッセージは作業内容がわかるようにする
- Pull Request にはスクリーンショットを添付するなどし、作業内容を丁寧に記す(issueに紐づく作業はissue番号をつける）
- ダミー画像やコミットメッセージに砕けたものを使用しない

## ブランチ名

```
feat/<issue番号>
```

## コミットコメント

作業タイプ(type)、 作業範囲(scrope) タイトル、 関連するissue番号（ある場合）を盛り込んだ下記フォーマットとなります。typeはあらかじめ決まっているので、適したtypeを設定してください。Google仕様。Updateではこのルールに則ってコミットにコメントをつけてください。

形式:
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
|refactor|無駄な記述をスマートにしたりと、最適なコーディングに整える作業|
|perf|コードチューニングをし、処理パフォーマンスを改善する場合|
|test|テスト関連|
|chore|開発環境やCIなどコアなファイル群に関する作業|


## Tips

### Gitに含めないファイル

重いファイルなどは `.gitignore` ファイルに改行区切りで列挙してgitのコミット対象から外しましょう

```.gitignore
node_modules
.DS_Store
dist
```

### 直前のコミットメッセージを書き直す

```
git commit -a --amend
```

vimでコメントを編集、保存。

### コンフリクトした

修正する

### 作業前の状態に戻したい

```
git checkout .
```
