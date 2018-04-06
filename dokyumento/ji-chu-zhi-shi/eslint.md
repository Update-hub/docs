---
description: JSの品質チェックツール。必ず入れましょう。
---

# ESLint

## 公式ドキュメント

{% embed data="{\"url\":\"https://eslint.org/\",\"type\":\"link\",\"title\":\"ESLint - Pluggable JavaScript linter\",\"description\":\"A pluggable and configurable linter tool for identifying and reporting on patterns in JavaScript. Maintain your code quality with ease.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://eslint.org/img/favicon.512x512.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://eslint.org/img/favicon.512x512.png\",\"aspectRatio\":0}}" %}

## クイックスタート

{% tabs %}
{% tab title="ES5" %}
```bash
$ npm install --save-dev eslint-config-standard eslint-plugin-standard eslint-plugin-promise eslint-plugin-import eslint-plugin-node
```

{% code-tabs %}
{% code-tabs-item title=".eslintrc.json" %}
```javascript
{
  "extends": "standard"
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}
{% endtab %}

{% tab title="ES6" %}
```bash
$ npm install -D eslint eslint-config-google
```

{% code-tabs %}
{% code-tabs-item title=".eslintrc.json" %}
```javascript
{
    "extends": "google",
    "parserOptions": {
        "ecmaVersion": 6
    }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}
{% endtab %}
{% endtabs %}

## Tips

| 症状 | 対策 |
| --- | --- |
| google や $などが怒られる | `/* global google */` や `/* global $ */` をファイル先頭に記述 |



