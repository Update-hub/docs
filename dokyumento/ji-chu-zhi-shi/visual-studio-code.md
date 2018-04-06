# visual studio code

[https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx](https://www.microsoft.com/ja-jp/dev/products/code-vs.aspx)

* Emmetが内蔵されています。
* Gitが内蔵されています。（サイドバーよりcommit、 pushが可能）

## 設定ファイル

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

## ユーザースニペット

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

