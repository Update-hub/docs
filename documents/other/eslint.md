---
description: JSの品質チェックツール。必ず入れましょう。
---

# ESLint

## 公式ドキュメント

{% embed url="https://eslint.org/" %}

## クイックスタート

チーム開発の場合、

{% tabs %}
{% tab title="ES5" %}

```bash
npm install --save-dev eslint-config-standard eslint-plugin-standard eslint-plugin-promise eslint-plugin-import eslint-plugin-node
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
npm install -D eslint eslint-config-google
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

### Googleや $などが怒られる

`/* global google */` や `/* global */` をファイル先頭に記述