# ESLint

JSの品質チェックツール

## 事前準備

Visual Studio Code ESLint [https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

## 設定

### ES5

```bash
npm install --save-dev eslint-config-standard eslint-plugin-standard eslint-plugin-promise eslint-plugin-import eslint-plugin-node
```

.eslintrc.json をプロジェクトルートに作成し下記内容に変更

```javascript
{
  "extends": "standard"
}
```

### ES6

```bash
npm install -D eslint eslint-config-google
```

.eslintrc.json をプロジェクトルートに作成し下記内容に変更

```javascript
{
    "extends": "google",
    "parserOptions": {
        "ecmaVersion": 6
    }
}
```

## Tips

| 症状 | 対策 |
| --- | --- |
| google や $などが怒られる | `/* global google */` や `/* global $ */` をファイル先頭に記述 |

