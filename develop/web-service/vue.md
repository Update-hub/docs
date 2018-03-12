# Vue

https://jp.vuejs.org/index.html
https://vuex.vuejs.org/ja/
https://router.vuejs.org/ja/

## ESLint

Visual Studio CodeでESLintを **.Vue で適用させるためにはユーザー設定に下記の記載が必要。

```js
"eslint.validate": [
  "javascript", {
    "language": "vue",
    "autoFix": true
  }
]
```