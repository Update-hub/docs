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

## Tips

### If文

 条件分岐が使えます。

{% code-tabs %}
{% code-tabs-item title="sample.pug" %}
```javascript
- var pet = 'dog'

if pet === 'dog'
  p 犬
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="sample.html" %}
```markup
<p>犬</p>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### each文

 繰り返しの記述部分は配列とループ処理を使って書けます。

{% code-tabs %}
{% code-tabs-item title="sample.pug" %}
```javascript
- var list = ['cat', 'dog', 'pig']

ul
  each i in list
    li.pet= i
    // li.pet-list #{i}でも可
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="sample.html" %}
```markup
<ul>
  <li class="pet">cat</li>
  <li class="pet">dog</li>
  <li class="pet">pig</li>
</ul>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Mixin

 複数個所で呼び出す共通部を関数のように作成できます。 mixin用のファイルを別に作ることもできますが、同じファイル内にも記述できます。

{% code-tabs %}
{% code-tabs-item title="sample.pug" %}
```javascript
mixin pet(name)
  li.pet= name
  // li.pet #{name} でも可

ul
  +pet('cat')
  +pet('dog')
  +pet('pig')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

 `+mixin名()` で呼び出します。任意の値を引数に渡すことが可能です。

{% code-tabs %}
{% code-tabs-item title="sample.html" %}
```markup
<ul>
  <li class="pet">cat</li>
  <li class="pet">dog</li>
  <li class="pet">pig</li>
</ul>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

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

