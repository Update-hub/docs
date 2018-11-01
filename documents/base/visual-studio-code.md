---
description: 最も軽量なエディタ
---

# Visual Studio Code

## 概要

Visual Studio Code は Microsoft 社が開発している無料のテキストエディタです。従来のエディタに比べ非常に軽量で、拡張機能を使えば開発効率を大幅に向上させることができます。vscode と略されます。

{% embed url="https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx" %}

## よく使う操作

あらゆるツールに共通することとして、ショートカットの使い方を覚え、染み込ませましょう。単純に作業効率が2倍以上になります。

windows の方は下記を参考にしてください。

{% embed url="https://qiita.com/TakahiRoyte/items/cdab6fca64da386a690b" %}

### コマンドパレット\(⌘⇧P \)

あらゆるコマンドにアクセスすることができます。ステータスバーの `表示>コマンドパレット` から開くことができます。 通常はショートカットで開きます。ショートカットはOSによって異なるので、コマンド横の表記を覚えるようにしましょう。  
  
以後、各機能の説明ではコマンド名を記載するので、コマンドパレットでコマンドを検索して使用してください。その際、ショートカットがあるものは以降ショートカットで機能を実行しましょう。

### ソースコードの整形\(⇧⌥F\)

ソースコードの整形を行うことができます。

### 複数単語選択\(⌘D\)

ソース中の同じ単語や類似のタグを一括で編集したい場合に多用します。

### ファイルの切り替え\(⌘P\)

ファイルの切り替えで多用します。切り替えたいファイルやディレクトリを入力することで、直感的に目的のファイルを開くことができます。

### Diff

compare でコマンド検索をしてください。クリップボードや、開いている他のファイルと差分を確認することができます。

### 拡張機能\(⇧⌘K\)

拡張機能の検索、更新、削除ができます。

## 推奨拡張機能

### 各種言語系

PHP, TypeScript, Ruby など、各言語ごとの拡張機能があるので、目的に応じて導入しておきましょう。

### EditorConfig

複数人で開発する際、インデントの種類や量がブレないためにEditorConfigを使います。プロジェクトルートに .editorconfig ファイルを設置することで、editorconfig に対応したエディタで共通のインデントルールを用いることができます。

{% embed url="https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig" %}

### Beautify

コード整形を助けてくれます。

{% embed url="https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify" %}

### Git系

Gitログを見たり、GitHub, GItLabと連携する際に便利です。

{% embed url="https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory" caption="Git Logが見れます" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=fatihacet.gitlab-workflow" caption="GitLabの操作ができます" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens" caption="他の人の作業ログがソース上で確認できます" %}

### Lint系

{% embed url="https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=mkaufman.HTMLHint" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-puglint" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint" %}

### ローカルサーバー

{% embed url="https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=jasonlhy.vscode-browser-sync" caption="スマホチェックもしたい場合" %}

### その他補助系

{% embed url="https://marketplace.visualstudio.com/items?itemName=tomoki1207.vscode-input-sequence" caption="連番の入力が簡単になります" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils" caption="ファイルの作成、複製がコマンドパレットから可能になります" %}

{% embed url="https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager" caption="プロジェクト管理が可能になります" %}

## Tips

### コマンドからディレクトリ、ファイルをvscodeで開く

`$ code <ディレクトリ位置 or ファイル名>` のコマンドで、任意のディレクトリやファイルをルートとした状態でvscode を立ち上げることができます。

例えば、現在のディレクトリをルートとしてvscodeを立ち上げたい場合、以下のコマンドを叩きます。

```text
$ code ./
```

### 設定ファイル

おすすめ設定

QuickOpen\(`Cmd + P` or `Ctrl + p`\) からdistを除外

```text
"search.exclude": {
  "dist/**/*": true
},
```

Vue ファイルにESLintを適用

```text
  "eslint.validate": [
    "javascript",
    {
      "autoFix": true,
      "language": "vue"
    }
  ],
```

pugLint有効化（要PugLint拡張機能）

```text
"puglint.enable": true,
```

emmet\(inPug\)でattrをシングルクウォートに

```text
"pug": {
  "attr_quotes": "single"
}
```

emmetで展開されるhtmlのlangをjaに

```text
  "emmet.variables": {
    "lang": "ja"
  },
```

### ユーザースニペット

Visual Studio Codeではユーザー独自のスニペットを定義する事が出来ます。  
スニペットとはVisual Studio Codeで文字を打ち込むと下に出てきて、コードを楽に入力できる、スマホ等の予測変換のようなものです。

作成方法はメニューバーからファイル&gt;基本設定&gt;ユーザースニペットを選択、その後どの言語のスニペットを聞かれるので使用する物を選択します。  
例えばhtmlを選択するとhtml.jsonというファイルが開かれます。  
その中に定義することでそのスニペットが使えるようになります。

例えばjavascriptで「log」打ち込んで`console.log('');`を呼び出すような場合はこうなります。

```text
    "Print to console": {
        "prefix": "log",// "prefix"の値がスニペットを呼び出す際に使う文字列
        "body": [
            "console.log('$1');",// 改行する際は「,」を使う。 「$1」でこのスニペットを呼び出した際にこの位置から入力できるようになる。
            "$2"// 「$2」は「$1」の位置にいる時にtabキーを押すとそこに移動します。「$3」以降も同様。
        ],
        "description": "Log output to console"
    },
```

詳しくは下記のサイト等を見てください。

{% embed url="https://qiita.com/kz\_kazuki/items/d26946c1e7169847aeef" %}

{% embed url="https://vscode-doc-jp.github.io/docs/userguide/userdefinedsnippets.html" %}



