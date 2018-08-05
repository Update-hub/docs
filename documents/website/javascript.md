# JavaScript

## 概要

JavaScript\(JS\)はWebサイトの動的表現やデータベース通信に欠かせません。ただ書けるだけではなく、いかにメンテナブルに、軽量に記述できるかが鍵となります。

### 推奨教材

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/JavaScript\",\"type\":\"link\",\"title\":\"JavaScript\",\"description\":\"JavaScript \(JS\) は軽量で、軽量なインタプリタ型、あるいは JITコンパイルされる、 第一級関数 を備えたプログラミング言語です。Web ページでよく使用されるスクリプト言語として知られ、 node.js や Apache CouchDB や Adobe Acrobat といった 多くの非ブラウザー環境においても使用されています 。 JavaScript は プロトタイプベース で、動的型付けを持ち、そしてオブジェクト指向、命令形、宣言的 \(例えば関数プログラミング\) といったスタイルをサポートするマルチパラダイムのスクリプト言語です。詳しくは JavaScript について をお読みください。\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1},\"caption\":\"厳密には公式ドキュメントではない\"}" %}



### Style Guide

スペースルールなど、細かいルールをGoogleが提唱してくれています。[ESLint](../other/eslint.md)でも同様のルールを用いることができます。

{% embed data="{\"url\":\"https://google.github.io/styleguide/jsguide.html\",\"type\":\"link\",\"title\":\"Google JavaScript Style Guide\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.google.com/favicon.ico\",\"aspectRatio\":0},\"caption\":\"Update推奨\"}" %}

### Version

JSにはバージョンがある。ブラウザ対応状況の都合でいまだにES5が主流だが、Babelなどのコンパイラを使ってES6以降を採用する現場増えていいる。特に理由がなければ最新バージョンを使って開発を行いましょう。

{% embed data="{\"url\":\"https://developer.mozilla.org/ja/docs/Web/JavaScript/Language\_Resources\",\"type\":\"link\",\"title\":\"JavaScript 言語情報\",\"description\":\"ECMAScript は JavaScript の基礎を成すスクリプト言語です。ECMAScript は標準化団体 ECMA International によって ECMA-262 および ECMA-402 specifications として標準化されています。次のような ECMAScript 標準が承認済みおよび策定中です:\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/favicon144.e7e21ca263ca.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.mdn.mozilla.net/static/img/opengraph-logo.72382e605ce3.png\",\"width\":600,\"height\":600,\"aspectRatio\":1},\"caption\":\"バージョン一覧\"}" %}

{% embed data="{\"url\":\"http://kangax.github.io/compat-table/es6/\",\"type\":\"link\",\"title\":\"ECMAScript 6 compatibility table\",\"caption\":\"ブラウザ対応状況\"}" %}

## Tips

### ググりにくい記法

| `...object` | スプレッドオペレータ |
| :--- | :--- |
| `hoge ? a : b` | 三項演算子 |

### マークアップ

JSのフックとなるようなDOM要素には、別途 `js-xxx` というクラス名をつける。











