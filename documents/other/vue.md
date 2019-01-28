# Vue

## 公式ドキュメント

{% embed url="https://jp.vuejs.org" %}

{% embed url="https://vuex.vuejs.org/ja/" %}

{% embed url="https://router.vuejs.org/ja/" caption="" %}

## Tips

### ESLint

Visual Studio CodeでESLintを \*\*.Vueで適用させるためにはユーザー設定に下記の記載が必要。

```javascript
"eslint.validate": [
  "javascript", {
    "language": "vue",
    "autoFix": true
  }
]
"emmet.includeLanguages": {
    "vue-html": "html"
},
```

### vue-cli

vue-cliがあればコマンドひとつで開発環境を整えることができる。

{% embed url="https://github.com/vuejs/vue-cli" %}

## Nuxt.js

### チュートリアル

{% embed url="https://www.youtube.com/playlist?list=PLw1QAmLkyyah6k7NhCUqW48jAbUETumtO" caption="シリーズです" %}

公式サイトが非常によくまとまっている、

{% embed url="https://ja.nuxtjs.org/" caption="公式サイト" %}

{% embed url="https://deerboy.qrunch.io/entries/leNz4md8MM0mgwCy" caption="概要" %}

### 注意

scopedがないと全ページにスタイルが影響しますが、開発時はnuxt-linkで遷移しないと他ページに影響しません。最終的に静的生成するともちろん影響します。基本的には scoped で閉ざすのを推奨します。
