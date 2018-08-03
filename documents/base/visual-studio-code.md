---
description: 最も軽量なエディタ
---

# Visual Studio Code

## 概要

Visual Studio Code は Microsoft 社が開発している無料のテキストエディタです。従来のエディタに比べ非常に軽量で、拡張機能を使えば開発効率を大幅に向上させることができます。vscode と略されます。

{% embed data="{\"url\":\"https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx\",\"type\":\"link\",\"title\":\"Visual Studio Code - Visual Studio\",\"description\":\"Mac, Windows, Linux の軽量/高速な高機能開発エディター\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.microsoft.com/favicon.ico\",\"aspectRatio\":0}}" %}

## よく使う操作

あらゆるツールに共通することとして、ショートカットの使い方を覚え、染み込ませましょう。単純に作業効率が2倍以上になります。

windows の方は下記を参考にしてください。

{% embed data="{\"url\":\"https://qiita.com/TakahiRoyte/items/cdab6fca64da386a690b\",\"type\":\"link\",\"title\":\"【Windows版】VS Code キーボードショートカット一覧 （オススメ付き） - Qiita\",\"description\":\"VS Codeのデフォルトショートカット一覧です。 ★が付いているのは個人的なオススメです。  2016.11.08追記 メニューの ヘルプ > Keyboard Shortcuts Reference で英語版ですがキーボードショー...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.qiita.com/assets/favicons/public/apple-touch-icon-f9a6afad761ec2306e10db2736187c8b.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.qiita.com/assets/qiita-fb-2887e7b4aad86fd8c25cea84846f2236.png\",\"width\":200,\"height\":200,\"aspectRatio\":1}}" %}

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

### Beautify

コード整形を助けてくれます。

{% embed data="{\"url\":\"https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify\",\"type\":\"link\",\"title\":\"Beautify - Visual Studio Marketplace\",\"description\":\"Extension for Visual Studio Code - Beautify code in place for VS Code\",\"icon\":{\"type\":\"icon\",\"url\":\"https://marketplace.visualstudio.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://hookyqr.gallerycdn.vsassets.io/extensions/hookyqr/beautify/1.3.2/1528842959943/Microsoft.VisualStudio.Services.Icons.Default\",\"width\":256,\"height\":256,\"aspectRatio\":1}}" %}

### 

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
[https://qiita.com/kz\_kazuki/items/d26946c1e7169847aeef](https://qiita.com/kz_kazuki/items/d26946c1e7169847aeef)  
[https://vscode-doc-jp.github.io/docs/userguide/userdefinedsnippets.html](https://vscode-doc-jp.github.io/docs/userguide/userdefinedsnippets.html)

