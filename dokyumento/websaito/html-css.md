# HTML/CSS

## 公式ドキュメント

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/HTML\",\"type\":\"link\",\"title\":\"HTML\",\"description\":\"HTML \(HyperText Markup Language\) はウェブのもっとも基本的な構成要素です。 HTML はウェブページの基本レイアウトに従ってウェブページのコンテンツを記述し定義するものです。 HTML に隣接する他の技術としては、ウェブページの表示や表現を記述するもの \(CSS\) または機能や振る舞いを記述するもの \(JavaScript\) があります。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1},\"caption\":\"厳密には公式サイトではない\"}" %}

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/CSS\",\"type\":\"link\",\"title\":\"CSS: カスケーディングスタイルシート\",\"description\":\"Cascading Style Sheets（CSS）はスタイルシート言語であり、 HTML や XML （XHTML・SVG などを含む）で記述された文書の体裁や見栄えを表現するために用いられます。 CSS は、要素が画面上で（あるいは紙や音声といった別のメディア上で）どのように表現されるのかを定義します。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1},\"caption\":\"厳密には公式サイトではない\"}" %}

## Style Guide

{% embed data="{\"url\":\"https://google.github.io/styleguide/htmlcssguide.html\",\"type\":\"link\",\"title\":\"Google HTML/CSS Style Guide\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.google.com/favicon.ico\",\"aspectRatio\":0}}" %}

## Tips

### モバイルファースト

レスポンシブ実装を行う際、スマートフォンユーザー向けの実装をはじめに行い、次いでデスクトップユーザー向けの実装を行う手法をモバイルファーストと呼びます。これによりスマホユーザーはデスクトップユーザー向けのスタイルを読み込む必要がなくなり、低回線でも比較的快適なブラウジング体験が得られます。

以下の例でははじめにスマートフォン向けにボタンのスタイル実装を行い、デスクトップ向けのスタイル実装を後から実装しています。これによりスマートフォンユーザーはデスクトップ用の文字サイズ、行間の適用を行うことはありません。

```text
.button {
  font-size: 12px;
}

/* デスクトップ用スタイル */
@media screen and (min-width: 768px) {
  .button {
    font-size: 24px;
    line-height: 34px;
  }
}
```

ここで、

```text
@media screen and (min-width: 768px){}
```

の中に記述されたスタイルは画面の横幅が768px以上の場合に適用されます。

逆にデスクトップ用スタイルを書いたあとmax-width:767pxでスマートフォン用スタイルを書くというやり方をPCファーストと呼びます。この場合スマートフォンユーザーはデスクトップ用のスタイルを読み込んだ後さらにスマートフォン用のスタイルを読み込むことになり、表示が遅くなります。

モバイルファーストにはデザインもコーディングも含めたあらゆる設計を、スマートフォンユーザーを第一義に考えるという意味が含まれます。

###  セマンティックマークアップ

  `div`  `span` タグのみで文字をラップしたりすることは基本的にNGです。セマンティックなマークアップを心がけましょう。

{% embed data="{\"url\":\"https://developer.mozilla.org/en-US/docs/Glossary/Semantics\",\"type\":\"link\",\"title\":\"Semantics\",\"description\":\"In programing, Semantics refers to the meaning of a piece of code — for example \\"what effect does running that line of JavaScript have?\\", or \\"what purpose or role does that HTML element have\\" \(rather than \\"what does it look like?\\".\)\",\"icon\":{\"type\":\"icon\",\"url\":\"https://developer.mozilla.org/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://developer.mozilla.org/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1}}" %}

{% embed data="{\"url\":\"https://www.w3schools.com/html/html5\_semantic\_elements.asp\",\"type\":\"link\",\"title\":\"HTML5 Semantic Elements\",\"description\":\"Well organized and easy to understand Web building tutorials with lots of examples of how to use HTML, CSS, JavaScript, SQL, PHP, and XML.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.w3schools.com/favicon.ico\",\"aspectRatio\":0}}" %}



