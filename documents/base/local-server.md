---
description: 確認環境
---

# ローカルサーバー

## 概要

ルート相対のリンクが含まれるファイルを直接ブラウザで開くと、リンク切れを起こします。ルート相対の場合はプロジェクトルート（親）から見た位置で判断するので、プロジェクトのディレクトリを基点にサーバーを立ち上げないと、PCのルートが親の位置になるため、パスが通らずリンク切れを起こします。

## 起動方法

### Gulpの場合

Gulpを使ったサイトの場合、Browser-Syncなどのプラグインを使ってserveタスクを作成し、Gulpの中で起動するようにします。

### それ以外の場合

Gulpを使っていない場合、Serveというnpmコマンドをインストールすることで簡単にローカルサーバーが立てられるようになります。

{% embed data="{\"url\":\"https://www.npmjs.com/package/serve\",\"type\":\"link\",\"title\":\"serve\",\"description\":\"Static file serving and directory listing\",\"icon\":{\"type\":\"icon\",\"url\":\"https://static.npmjs.com/1996fcfdf7ca81ea795f67f093d7f449.png\",\"width\":230,\"height\":230,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://static.npmjs.com/338e4905a2684ca96e08c7780fc68412.png\",\"width\":1200,\"height\":630,\"aspectRatio\":0.525}}" %}

プロジェクトディレクトリで serve コマンドを叩くことでその位置をルートとしてローカルサーバーを立ち上げることができます。起動時に表示される外部向けURLを同一Wifiのスマートフォンで開くことで実機チェックもできます。

別のオプションとして、Visual Studio Code の Live Server を使う方法があります。

{% embed data="{\"url\":\"https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer\",\"type\":\"link\",\"title\":\"Live Server - Visual Studio Marketplace\",\"description\":\"Extension for Visual Studio Code - Launch a development local Server with live reload feature for static & dynamic pages\",\"icon\":{\"type\":\"icon\",\"url\":\"https://marketplace.visualstudio.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://ritwickdey.gallerycdn.vsassets.io/extensions/ritwickdey/liveserver/5.1.1/1529500150547/Microsoft.VisualStudio.Services.Icons.Default\",\"width\":256,\"height\":256,\"aspectRatio\":1}}" %}

この拡張機能場合ファイルの更新がオートリロードで反映されます。

