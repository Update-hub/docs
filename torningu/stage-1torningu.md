# stage-1:基礎トレーニング

## 概要

このトレーニングでは既存サイトのメンテナンスを通して、実務の基本的な流れを身につけます。

* 既存のソースコードに修正を加えること
* 作業の保存とソースコードのレビュー依頼、修正対応
* 正しいコードの書き方

## チュートリアル

{% embed data="{\"url\":\"https://youtu.be/sY64kVwQ-bw\",\"type\":\"video\",\"title\":\"gitによる共同開発\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/sY64kVwQ-bw/maxresdefault.jpg\",\"width\":1280,\"height\":720,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/sY64kVwQ-bw?rel=0&showinfo=0\",\"html\":\"<div style=\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\"><iframe src=\\"https://www.youtube.com/embed/sY64kVwQ-bw?rel=0&amp;showinfo=0\\" style=\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\" allowfullscreen scrolling=\\"no\\"></iframe></div>\",\"aspectRatio\":1.7778},\"caption\":\"Gitによる共同開発\"}" %}

{% page-ref page="../document/basic/buranchi.md" %}

## 準備

1. [課題](https://classroom.github.com/a/aK4sv0P7)リポジトリの作成
2. 課題リポジトリをクローンして開発を行ってください。

```bash
git clone <自分のリポジトリURL>
cd <自分の課題ディレクトリ>
npm i // しばらく待つ
gulp serve
```

* 上記コマンドで開発環境が構築され、確認用URLが自動的に開きます。
* 開発中はソースコードの修正がリアルタイムに反映されます。
* `ctrl + c` を押すと開発を終了できます。

## 課題

1. [issue](https://github.com/Update-hub/foundation/issues)ごとにブランチを作成\(feature/【issue番号】\)し、対応後Pull Requestを作成してください。（自分ではマージしないでください）
2. 全てのPull Requestが通過したらクリアとなります。

### ポイント

* Pull Request 作成時は reviewer に自分以外のメンバーを設定してください。
* コミットメッセージは作業内容が端的にわかるようにしてください。また、紐付くissue番号を記載してください。　例：（`タイトルの文字サイズを大きく #23`）

