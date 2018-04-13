---
description: GitHub Flow に準拠しています。
---

# ブランチ管理

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
