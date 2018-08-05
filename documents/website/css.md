---
description: Webデザインの基本スキル
---

# CSS

## 概要

CSSはHTML同様極めて基本的なスキルであり、極めて重要な存在です。CSSはWebサイト制作において最も工数に影響する作業なので、CSSスタイリングの効率化はWebコーダーにとって必須スキルとなります。

HTML同様、複雑なスタイルへの対応やメンテンス性向上の目的からSCSS\(SASS\)といった拡張言語が用いられます。現状ほぼすべての現場でSCSSが採用されているため、CSSと合わせてSCSSや開発環境の理解が必須となります。

### 推奨ドキュメント

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/CSS\",\"type\":\"link\",\"title\":\"CSS: カスケーディングスタイルシート\",\"description\":\"Cascading Style Sheets（CSS）はスタイルシート言語であり、 HTML や XML （XHTML・SVG などを含む）で記述された文書の体裁や見栄えを表現するために用いられます。 CSS は、要素が画面上で（あるいは紙や音声といった別のメディア上で）どのように表現されるのかを定義します。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1}}" %}

## SCSS\(SASS\)

SCSSはSASSの記法の一つで、大きな括りとしてはSASSになります。書き方が違うだけで、基本的にはSCSS=SASSだと思ってください。SCSSを使うことで、CSSではできなかった以下のことが可能になります。

* 複数ファイル管理（CSSを複数ファイルに分割して管理できる）
* 変数の利用（色やサイズなど使いまわせる値を変数化できる）
* ネスト記法（入れ子の表現やBEMをシンプルに直感的にできる）

{% embed data="{\"url\":\"https://dotinstall.com/lessons/basic\_sass\",\"type\":\"link\",\"title\":\"Sass/SCSS入門 \(全15回\)\",\"description\":\"CSSを効率的に書くための記法であるSass/SCSSについて学んでいきます。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://dotinstall.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://dotinstall.com/package\_img/basic\_sass/screen\_1.png\",\"width\":640,\"height\":360,\"aspectRatio\":0.5625}}" %}

### 利用上の注意

SCSSは便利で多機能な反面、mixinやextendsを多用しすぎるとむしろ複雑になり、開発コストが上がることがあります。開発環境を属人化させないためにも、複数ファイル管理など最低限の利用に留めることも重要です。特にBEMによるコンポーネント設計が一般的になっている現在、mixinの使用が必要になるシーンはほとんどありません。

### SMACSS

SCSSファイルは複数ファイル管理を前提として使われるため、その管理ルールがプロジェクト単位で決められていることがあります。SMACSSは最も有名な管理ルールで、多くの現場で採用されています。SMACSSはディレクトリ構成の提唱以外にもBEMのようなコンポーネント設計手法の提唱も行なっていますが、多くの場合コンポーネント設計はBEM、ディレクトリ構成はSMACSSというハイブリッドな採用がなされます。（SMACSSが採用される場合）

以下はSMACSSのディレクトリ構成例です。

```text
+-layout/
| +-grid.scss
| +-alternate.scss
+-module/
| +-callout.scss
| +-bookmarks.scss
| +-btn.scss
| +-btn-compose.scss
+-base.scss
+-states.scss
+-site-settings.scss
+-mixins.scss
```

## BEM

最もメジャーなCSS命名規則です。CSS命名規則がない場合、無秩序なスタイル設計になりメンテナンス上大きなネックとため、基本的にはBEMでCSS命名を行うようにしましょう。

{% page-ref page="bem.md" %}

## 注意点

ビギナーにありがちな失敗例です。

### position: absolute の多用

position: absolute は自由に配置できるので便利な反面、RWD（レスポンシブ）においては融通が利かないためよほどのケースがないと用いられることはありません。横並びなどは `flex` を用いるようにし、基本的なレイアウト配置でposition: absolute を乱用するのはやめましょう。

### !importantの使用

BEMにのっとってコンポーネント指向で設計する限り、 `!important` が必要になることはありません。`!important` を使うことでJSによるスタイル更新や、modifier によるスタイル切り替えができなくなるため、**絶対に使わない**ようにしましょう。

### 同じスタイルを量産する

ほぼまったく同じのスタイルを複数Classにコピーしている場合、それらの共通箇所はコンポーネントとして切り離せないかを検討しましょう。例えば色違いのボタンがある場合は、ボタンというコンポーネントを作成し、色を切り替えるmodifier を用意する方が効率的です。

## 品質チェック

### W3C CSS Validation

下記サイトにURLやコード全体を貼り付け、エラーがない状態であれば、少なくとも構文的には正しいスタイリングであると言えます。

{% embed data="{\"url\":\"https://jigsaw.w3.org/css-validator/\",\"type\":\"link\",\"title\":\"The W3C CSS Validation Service\",\"icon\":{\"type\":\"icon\",\"url\":\"https://jigsaw.w3.org/favicon.ico\",\"aspectRatio\":0}}" %}

### Mobile-Friendly

下記サイトにURLを貼り付け、エラーがなければスマホ対応が適切なスタイリングであると言えます。

{% embed data="{\"url\":\"https://search.google.com/test/mobile-friendly\",\"type\":\"link\",\"title\":\"Mobile-Friendly Test - Google Search Console\",\"icon\":{\"type\":\"icon\",\"url\":\"https://ssl.gstatic.com/search-console/scfe/logo\_dark\_2x-037666dffd9635fa9092b132a2f49da5.png\",\"width\":452,\"height\":48,\"aspectRatio\":0.10619469026548672}}" %}

