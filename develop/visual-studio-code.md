# Visual Studio Code

https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx

- Emmetが内蔵されています。
- Gitが内蔵されています。（サイドバーよりcommit、 pushが可能）

## 設定ファイル

```json
{
  "git.enableSmartCommit": true,
  "search.exclude": {
    "dist/**/*": true
  },
  "window.zoomLevel": 0,
  "editor.tabSize": 2,
  "explorer.confirmDragAndDrop": false,
  "editor.minimap.enabled": false,
  "git.autofetch": true,
  "eslint.validate": [
    "javascript",
    {
      "autoFix": true,
      "language": "vue"
    }
  ],
  "puglint.enable": true,
  "emmet.variables": {
    "lang": "ja"
  },
  "emmet.syntaxProfiles": {
    "pug": {
      "attr_quotes": "single"
    }
  }
}
```