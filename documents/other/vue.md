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
