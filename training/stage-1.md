# Stage-1: 基礎トレーニング

このトレーニングでは既存サイトのメンテナンスを通して、実務の基本的な流れを身につけます。

## チュートリアル

- [Git操作](https://drive.google.com/drive/u/0/folders/0BwhcbXxSdjGibFRtZDlFcFBmV1E)
- [Git](/develop/git.html)
- [Gulp](/develop/web-service/gulp.html)

## 準備

1. [課題](https://classroom.github.com/a/aK4sv0P7)リポジトリの作成
2. 課題リポジトリをクローンして開発を行ってください。

```bash
git clone <自分のリポジトリURL>
cd <自分の課題ディレクトリ>
npm i // しばらく待つ
gulp serve
```

- 上記コマンドで開発環境が構築され、確認用URLが自動的に開きます。
- 開発中はソースコードの修正がリアルタイムに反映されます。
- `ctrl + c` を押すと開発を終了できます。

## 課題

1. [issue](https://github.com/Update-hub/foundation/issues)ごとにブランチを作成(feature/【issue番号】)し、対応後Pull Requestを作成してください。
2. 全てのPull Requestが通過したらクリアとなります。

### ポイント

- Pull Request 作成時は reviewer に自分以外のメンバーを設定してください。
- コミットメッセージは作業内容が端的にわかるようにしてください。