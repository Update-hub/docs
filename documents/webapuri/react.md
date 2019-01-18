---
description: Webアプリ開発のスタンダード
---

# React

## 公式ドキュメント

{% embed url="https://reactjs.org/" caption="React" %}

{% embed url="https://reacttraining.com/react-router/" caption="React Router" %}

{% embed url="https://redux.js.org/" caption="Redux" %}

## クイックスタート

{% hint style="info" %}
事前に[Yarn](https://yarnpkg.com/lang/ja/)のインストールを行ってください。
{% endhint %}

React Create Appの導入（まだの場合）

```bash
npm install -g create-react-app
```

Reactアプリを作成

```bash
create-react-app <アプリ名>
cd <アプリ名>
```

Redux, Routerを導入

```bash
yarn add redux react-redux react-router-dom
```

ESLintを導入\(オプション）

{% code-tabs %}
{% code-tabs-item title="eslintrc.json" %}

```javascript
{
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "rules": {
        "semi": [2, "always"]
    }
}
```

{% endcode-tabs-item %}
{% endcode-tabs %}

開発スタート

```text
yarn start
```

srcディレクトリ内に以下のディレクトリを作成してください。

| ディレクトリ名 | 役割 |
| :--- | :--- |
| reducers | reducerを格納\(redux\) |
| actions | reducerを格納\(redux\) |
| containers | containerをラップし、actions,reducersと接続\(redux\) |
| components | ページやユニークなコンポーネントを格納 |
| components/ui | 見出し、カードなど再利用可能なコンポーネントを格納 |

###  Example

{% embed url="https://github.com/Update-hub/sw-vote" %}

## Tips

### GitHub Pagesに公開

gh-pagesをプロジェクトに追加

```bash
yarn add -D gh-pages
```

package.jsonに3箇所記述を追加

{% code-tabs %}
{% code-tabs-item title="package.json" %}

```javascript
"private": true
"homepage": "GitHub Pages のURL", // ← 追加

~
"scripts": {
...
"predeploy": "npm run build", // ← 追加
"deploy": "gh-pages -d build" // ← 追加
}
```

{% endcode-tabs-item %}
{% endcode-tabs %}

deploy実行

```bash
yarn run deploy
```

GitHub Pagesの設定画面でブランチをgh-pagesに設定します。

![](../../.gitbook/assets/sukurnshotto-2018-04-12-170556.png)

しばらく待つか、設定後に再度何かしらのdeployを行うことで見れるようになります。