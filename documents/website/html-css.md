---
description: Webサイト制作の基本
---

# HTML

## 概要

HTMLはサイト制作における基本中の基本です。HTMLでサイトを組み立てることを一般的にマークアップと呼びます。マークアップ一つでSEOや検索画面での見え方、メンテナンス性が大きく左右されるため、非常に重要なスキルとなります。

昨今はReactやVue, WordPress の台頭によりHTMLをそのまま記述する機会が減りつつあります。静的サイト制作においても、静的サイトジェネレータやPug, EJS などのテンプレート言語とGulpを組み合わせてプログラマブルに組むシーンが増えています。したがって、これからのコーダーは正しいマークアップに加え、それらの開発環境も合わせて理解する必要があるのです。

### 推奨教材

まずは下記のサイトでHTML/CSSの基本を学んでください。

{% embed url="https://developer.mozilla.org/ja/docs/Web/HTML" caption="厳密には公式サイトではない" %}

{% embed url="https://hail2u.net/documents/html-best-practices.html" %}

### Style Guide

インデントルールなど細かいスタイルガイドをGoogleが提唱してくれています。

{% embed url="https://google.github.io/styleguide/htmlcssguide.html" %}

## 正しいマークアップ

見た目の表現はCSSで管理されるため、見た目だけで言えばすべて `div` タグで組むことも可能です。ただし、HTMLのタグにはそれぞれ意味、役割が存在し、それぞれに適したタグを使うことでSEO上有利になり、外部からコンテンツの構造を取得しやすくなります。

{% embed url="https://developer.mozilla.org/ja/docs/Web/HTML/Element" %}

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

{% embed url="https://dotinstall.com/lessons/basic\_emmet\_v2" %}

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

{% embed url="https://validator.w3.org/" %}

### PageSpeed Insights

下記サイトにURLを貼り付け、グリーンスコアであれば表示速度的に及第点と言えます。

{% embed url="https://developers.google.com/speed/pagespeed/insights/" %}

### Mobile-Friendly

下記サイトにURLを貼り付け、エラーがなければスマホ対応が適切なマークアップであると言えます。

{% embed url="https://search.google.com/test/mobile-friendly" %}

