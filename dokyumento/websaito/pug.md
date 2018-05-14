# Pug

## 概要

Pugを使うと、HTMLではできなかった以下のようなことができます。

* 共通のコンポーネントをインクルードして使いまわせる
* HTMLの記述を簡略化できる（閉じタグ忘れの防止、タイピング量の軽減）

Pugは非常に簡単です。HTMLとPugの大きな違いはありません。HTMLタグの後に半角スペースを入力し、内容を入力することでHTMLのタグと同じ意味になります。また、HTMLの入れこは半角スペース2つのインデントで表現します。基本的なPugの動作はたったこれだけです。

{% code-tabs %}
{% code-tabs-item title="sample.html" %}
```markup
<p>パラグラフ</p>
<ul>
  <li>リスト</li>
  <li>リスト</li>
  <li>リスト</li>
</ul>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="sample.pug" %}
```text
p パラグラフ
ul
  li リスト
  li リスト
  li リスト
```
{% endcode-tabs-item %}
{% endcode-tabs %}

さらに、If文やeach文、mixinが使えるのでよりプログラマブルにHTMLを記述することができ、大規模サイトの実装を効率化することができます。

{% hint style="info" %}
Pugと同じようにejs, handlebars, slim などもテンプレート言語として人気です。
{% endhint %}

### なぜテンプレート言語が必要なのか

たとえばあなたが100ページあるサイトを実装するとします。100ページの中にはヘッダー、フッター、サイドバーなど共通するコンポーネントが必ず存在します。Pugなどのテンプレート言語を使わない場合、100ページすべてのHTMLにそれらのコンポーネントをコピーする必要があります。それだけでなく、もしヘッダーに修正が入った場合、100ページすべてのヘッダーを修正する必要があります。

Pugの場合は、そういった再利用可能なコンポーネントを個別のインクルードファイルとして作成できます。例えば作成したヘッダーコンポーネントは、必要なページでincludeするだけで使いまわせるようになります。

## クイックスタート



## Tips

### インラインスタイルを入力したい

ふた通りの書き方があります。まずは普通にHTMLタグで記述する方法です。

```text
p 文章の中で<strong>ここだけ文字を大きく<strong>する。
```

次に文章用のPug記述を使い、個別に指定する方法です。

```text
p
  | 文章の中で
  strong ここだけ文字を大きく
  | する。 
```

### 軽微なネスト（入れ子）を省略する

`:(半角スペース)` で区切ることでネスト（入れ子）にすることができます。

```text
p: a(href='') リンク
```

### PugLint を有効にする

pug-lintをインストール

```bash
$ npm i -g pug-lint
```

Visual Studio Code のユーザー設定に以下の記述を追加。

```javascript
"puglint.enable": true,
"pug": {
  "attr_quotes": "single"
}
```

`.pug-lintrc.json` をプロジェクトルートに作成（ない場合）

{% code-tabs %}
{% code-tabs-item title=".pug-lintrc.json" %}
```javascript
{
  "validateIndentation": 2,
  "validateAttributeQuoteMarks": "'",
  "validateAttributeSeparator": { "separator": " ", "multiLineSeparator": "\n " },
  "validateDivTags": true,
  "requireStrictEqualityOperators": true,
  "requireSpecificAttributes": [ { "img": [ "alt" ] } ],
  "requireSpaceAfterCodeOperator": [ "-", "=", "!=" ],
  "requireLowerCaseTags": true,
  "requireLowerCaseAttributes": true,
  "requireLineFeedAtFileEnd": true,
  "requireIdLiteralsBeforeAttributes": true,
  "requireClassLiteralsBeforeAttributes": true,
  "disallowSpacesInsideAttributeBrackets": true,
  "disallowMultipleLineBreaks": true,
  "disallowLegacyMixinCall": true,
  "disallowIdAttributeWithStaticValue": true,
  "disallowClassLiteralsBeforeIdLiterals": true,
  "disallowClassAttributeWithStaticValue": true
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

[puglint](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-puglint) の拡張機能をインストールすると、Lintが有効になり、Pugの記述にエラーが表示されるようになります。

