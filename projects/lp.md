---
description: 本格的な制作の入門
---

# LP

## 概要

{% embed url="https://www.youtube.com/playlist?list=PLw1QAmLkyyagERb4oKAahzmziVMfHZrPq"　caption="動画はシリーズになっています" %}

LP（ランディングページ）は初期フェーズでもっとも多い案件の種類です。商品やサービスを訴求するための縦長のサイトで、通常1ページで構成されます。1ページとはいえデザインや動きが凝っていることが多く、Webサイト制作に必要なスキルがひととおり必要になります。

### 妥当工数

15人日\(90H\)以下

## チュートリアル

このプロジェクトを進める前に、事前に以下のドキュメントを読んでください。

{% page-ref page="../documents/website/" %}

本プロジェクトではGulpの設計と準備が終わっているので、Gulpについての理解は不要です。READMEに沿ってコマンドで開発環境構築を行ってください。

### ポイント

* h1やpなどのタグにスタイルを付与しない。かならずclassに対してスタイルをつける。
* JSでクリックイベントを付与するタグには`.js-xxx`のようにjsプレフィックスをつける。
* 作業後はVisual Studio Codeでフォーマットをかけてコードを整形する。
* class名は意味がわかるものにする。`class="p"`や`class="red"`ではなく、`class="text"`や`class="error"`とする。
* `-webkit-`などのブラウザ用プレフィックスは不要（ほとんどのタグが標準で動くため）

## プロジェクトファイル

lp-XXXX（XXXXは自分の名前）として自分のGitLabグループにインポートして、作業を開始してください。プロジェクトの進めかたは[こちら](flow.md)をご参照ください。

{% embed url="https://drive.google.com/drive/folders/1cmn5mw5mYDcWOn\_XGr4b1QQcMoW3EfaZ" %}

Fontはすべて [Raleway](https://fonts.google.com/specimen/Raleway) を使ってください。\(PSD上でRaleway以外の部分も、RalewayでOKです）
