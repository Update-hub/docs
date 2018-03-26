# Visual Studio Code

https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx

- Emmetが内蔵されています。
- Gitが内蔵されています。（サイドバーよりcommit、 pushが可能）

## 設定ファイル

おすすめ設定

QuickOpen(`Cmd + P` or `Ctrl + p`) からdistを除外

```
"search.exclude": {
  "dist/**/*": true
},
```

Vue ファイルにESLintを適用  
```
  "eslint.validate": [
    "javascript",
    {
      "autoFix": true,
      "language": "vue"
    }
  ],
```

pugLint有効化（要PugLint拡張機能）
```
"puglint.enable": true,
```

emmet(inPug)でattrをシングルクウォートに
```
"pug": {
  "attr_quotes": "single"
}
```
emmetで展開されるhtmlのlangをjaに
```
  "emmet.variables": {
    "lang": "ja"
  },
```