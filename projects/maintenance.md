---
description: 既存サイトのメンテナンス
---

# メンテナンス

## 概要

現場で最初にやるのは修正作業です。既存の開発環境をインストールし、指示に沿って修正作業を行ってください。修正作業を通してGitやエディターの操作、GitLabのワークフローを身につけてください。

各作業ブランチは必ず**masterから**作成します。ブランチは通常現在のブランチを元に作られます。（作成時に元となるブランチを指定する方法もありますが）たとえばAの作業を行ったブランチにいる状態でブランチBを作成すると、Aの作業を含んだブランチBが誕生します。Aにバグが潜んでいた場合、バグがブランチBにも引き継がれます。また、その状態でブランチBのマージリクエストを出すとコードの差分にAの作業も含まれるため、レビューにも支障をきたします。

### 妥当工数

2人日\(16H\)以下

## チュートリアル

このプロジェクトを進めるには事前に以下のドキュメントを読んでください。

{% page-ref page="../documents/base/" %}

### 基礎スキルの習得

以下のサイトで基礎スキルの習得を行ってください。

#### Progate

<https://prog-8.com/languages>

以下のコースをクリアする（無料範囲のみでOK）

* HTML
* CSS
* JavaScript
* jQuery
* Command Line
* Git
* Sass
* [Develoer Tool の使い方](https://prog-8.com/docs/html-dev)

#### Dotinsall

以下の動画を確認する

* https://dotinstall.com/lessons/basic_html_v4
* https://dotinstall.com/lessons/basic_css_v4
* https://dotinstall.com/lessons/website_html_v3
* https://dotinstall.com/lessons/basic_javascript_v3
* https://dotinstall.com/lessons/basic_chrome_dev_v2
* https://dotinstall.com/lessons/basic_emmet_v2
* https://dotinstall.com/lessons/basic_git
* https://dotinstall.com/lessons/basic_sass

## ポイント

* MR画面でDiffを確認する。その課題に関係ない別の課題の作業が紛れ込んでいない状態にする。
* レビューで指摘があった場合、そのブランチで再度対応したあとそのままPushすれば良い。MRを出し直す必要はない。

## プロジェクトファイル

maintenance-XXXX（XXXXは自分の名前）として自分のGitLabグループにインポートして、作業を開始してください。プロジェクトの進めかたは[こちら](flow.md)をご参照ください。

{% embed url="https://drive.google.com/open?id=1Rv1SiTSDa0lT2AWs1\_\_ti11BdWYWaW37" %}

プロジェクトのインポート後は、下記動画部分を参考にリポジトリ操作の通知がチームチャンネルに飛ぶように設定してください。

{% embed url="https://youtu.be/CHb4TdHX7fw?t=87" %}
