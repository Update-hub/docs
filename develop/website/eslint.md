# ESLint

Visual Studio Code ESLint
https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint



```bash
npm install -D eslint eslint-config-google
```

.eslintrc.json をプロジェクトルートに作成し下記内容に
```json
{
    "extends": "google",
    "parserOptions": {
        "ecmaVersion": 6
    }
}
```

以後JSにLintが適用される。