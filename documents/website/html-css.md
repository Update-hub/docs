---
description: Webサイト制作の基本
---

# HTML

## 概要

HTMLはサイト制作における基本中の基本です。HTMLでサイトを組み立てることを一般的にマークアップと呼びます。マークアップ一つでSEOや検索画面での見え方、メンテナンス性が大きく左右されるため、非常に重要なスキルとなります。

昨今はReactやVue, WordPress の台頭によりHTMLをそのまま記述する機会が減りつつあります。静的サイト制作においても、静的サイトジェネレータやPug, EJS などのテンプレート言語とGulpを組み合わせてプログラマブルに組むシーンが増えています。したがって、これからのコーダーは正しいマークアップに加え、それらの開発環境も合わせて理解する必要があるのです。

### 推奨教材

まずは下記のサイトでHTML/CSSの基本を学んでください。

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/HTML\",\"type\":\"link\",\"title\":\"HTML\",\"description\":\"HTML \(HyperText Markup Language\) はウェブのもっとも基本的な構成要素です。 HTML はウェブページの基本レイアウトに従ってウェブページのコンテンツを記述し定義するものです。 HTML に隣接する他の技術としては、ウェブページの表示や表現を記述するもの \(CSS\) または機能や振る舞いを記述するもの \(JavaScript\) があります。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1},\"caption\":\"厳密には公式サイトではない\"}" %}

{% embed data="{\"url\":\"https://hail2u.net/documents/html-best-practices.html\",\"type\":\"link\",\"title\":\"普通のHTMLの書き方\",\"icon\":{\"type\":\"icon\",\"url\":\"https://hail2u.net/apple-touch-icon-precomposed.png\",\"aspectRatio\":0}}" %}

### Style Guide

インデントルールなど細かいスタイルガイドをGoogleが提唱してくれています。

{% embed data="{\"url\":\"https://google.github.io/styleguide/htmlcssguide.html\",\"type\":\"link\",\"title\":\"Google HTML/CSS Style Guide\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.google.com/favicon.ico\",\"aspectRatio\":0}}" %}

## 正しいマークアップ

見た目の表現はCSSで管理されるため、見た目だけで言えばすべて `div` タグで組むことも可能です。ただし、HTMLのタグにはそれぞれ意味、役割が存在し、それぞれに適したタグを使うことでSEO上有利になり、外部からコンテンツの構造を取得しやすくなります。

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/HTML/Element\",\"type\":\"link\",\"title\":\"HTML 要素リファレンス\",\"description\":\"このページでは、タグを使用して作成されるすべての HTML 要素を一覧表示しています。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://developer.mozilla.org/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://developer.mozilla.org/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1}}" %}

### 初学者が犯すミス

#### 文章もdivで組んでしまう

divはレイアウトに用いる中性的なタグなので、基本的に文字や画像を `div` で直接wrap（囲む）ことはありません。文章や画像は `p` や `img` などで組みましょう。

#### brタグを多用する

見た目上の改行はcssで表現すべきです。文章の途中で文脈として意味もなく改行させる場合にbrを用いるのは間違いです。そういった場合には `<span>`で該当箇所を囲み、 `display: block;` などとします。

#### altタグを空にする

imgタグには構文ルールとしてaltタグが必須なので、altタグは必ず付与します。それに加え、**画像にテキストが含まれる場合**は必ずaltタグにテキストの内容を記述します。検索エンジンは画像に含まれるテキストが解析できないため、altタグの値を参照するためです。また、目が見えない方はスクリーンリーダーというブラウザ読み上げ機能でサイトを理解するのですが、altに文字が入っていないと、画像に含まれる文字が伝わりません。

特に、「お問い合わせはこちら 0120-xxx-xxx」などの極めて重要な情報が画像バナーになっていた場合、必ずaltにテキストを記入しましょう。

## BEM

HTMLのClass名は自由につけられますが、チームでClass命名規則を揃えないとメンテナンス上支障があります。現時点でBEMは最も多くの現場で採用されるClass命名規則です。

{% page-ref page="bem.md" %}

## Emmet

HTMLは記述量が非常に多いため、エディタのショートカットやスニペットの活用が効率化に非常に有効です。Emmetを使うと、わずかな記述でマークアップを効率的に進めることができます。Visual Studio Code にははじめから Emmet が内蔵されています。

{% embed data="{\"url\":\"https://dotinstall.com/lessons/basic\_emmet\_v2\",\"type\":\"link\",\"title\":\"Emmet入門 \(全15回\)\",\"description\":\"HTML/CSSを効率的にコーディングできるEmmet記法について学んでいきます。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://dotinstall.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://dotinstall.com/package\_img/basic\_emmet\_v2/screen\_1.png\",\"width\":640,\"height\":360,\"aspectRatio\":0.5625}}" %}

#### Emmet で BEM を使う

EmmetではBEMの出力も可能です。下記のようにbemフィルターを用います。

```markup
.hero>.-msg|bem
```

とすることで下記のHTMLマークアップが行えます。

```markup
<div class="hero">
  <div class="hero__msg"></div>
</div>
```

## テンプレート言語

ヘッダーやフッターなど、全ページ共通のコンポーネント（パーツのこと）を全ページにコピーするのは賢い方法とは言えません。構築後に共通部分に修正が入った場合、全ページのマークアップを変更する必要があるからです。

静的サイト制作においては、そういった共通パーツの流用を主な目的としてテンプレート言語が用いられます。テンプレート言語はHTMLを拡張した言語で、HTMLではできなかった変数の利用や別HTMLのインポートが可能になります。PugやEJSなどいくつか存在しますが、基本的な概念はどれも同じです。

{% page-ref page="pug.md" %}

テンプレート言語は便利な反面、関数や変数を多用すると逆に分かりづらくなり、開発環境が属人化しやすいため、複数ファイル管理など最低限の利用が推奨されます。

## 品質チェック

### W3C Markup Validation

下記サイトにURLやコード全体を貼り付け、エラーがない状態であれば、少なくとも構文的には正しいマークアップであると言えます。

{% embed data="{\"url\":\"https://validator.w3.org/\",\"type\":\"link\",\"title\":\"The W3C Markup Validation Service\",\"description\":\"W3C\'s easy-to-use       markup validation service, based on SGML and XML parsers.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://validator.w3.org/images/favicon.ico\",\"aspectRatio\":0}}" %}

### PageSpeed Insights

下記サイトにURLを貼り付け、グリーンスコアであれば表示速度的に及第点と言えます。

{% embed data="{\"url\":\"https://developers.google.com/speed/pagespeed/insights/\",\"type\":\"link\",\"title\":\"PageSpeed Insights\",\"icon\":{\"type\":\"icon\",\"url\":\"https://developers.google.com/favicon.ico\",\"aspectRatio\":0}}" %}

### Mobile-Friendly

下記サイトにURLを貼り付け、エラーがなければスマホ対応が適切なマークアップであると言えます。

{% embed data="{\"url\":\"https://search.google.com/test/mobile-friendly\",\"type\":\"link\",\"title\":\"Mobile-Friendly Test - Google Search Console\",\"icon\":{\"type\":\"icon\",\"url\":\"https://ssl.gstatic.com/search-console/scfe/logo\_dark\_2x-037666dffd9635fa9092b132a2f49da5.png\",\"width\":452,\"height\":48,\"aspectRatio\":0.10619469026548672}}" %}

