---
description: Webサイト制作における最重要スキル
---

# JavaScript

## 概要

JavaScript\(JS\)はWebサイトの動的表現やデータベース通信に欠かせません。ただ書けるだけではなく、いかにメンテナブルに、軽量に記述できるかが鍵となります。

### 推奨教材

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript" caption="厳密には公式ドキュメントではない" %}

### Style Guide

スペースルールなど、細かいルールをGoogleが提唱してくれています。[ESLint](../other/eslint.md)でも同様のルールを用いることができます。

{% embed url="https://google.github.io/styleguide/jsguide.html" caption="Update推奨" %}

### Version

JSにはバージョンがある。ブラウザ対応状況の都合でいまだにES5が主流だが、Babelなどのコンパイラを使ってES6以降を採用する現場増えていいる。特に理由がなければ最新バージョンを使って開発を行いましょう。

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Language\_Resources" caption="バージョン一覧" %}

{% embed url="http://kangax.github.io/compat-table/es6/" caption="ブラウザ対応状況" %}

## Tips

### ググりにくい記法

| `...object` | スプレッドオペレータ |
| :--- | :--- |
| `hoge ? a : b` | 三項演算子 |

### マークアップ

JSのフックとなるようなDOM要素には、別途 `js-xxx` というクラス名をつける。











