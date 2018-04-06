# OGP

OGPタグを設置するとSNSでURLをシェアした際、タイトルやサムネイルが表示されるようになります。

[公式ドキュメント](http://ogp.me)

```markup
<meta property="og:title" content="OGPのタイトル">
<meta property="og:description" content="OGPのディスクリプション">
<meta property="og:url" content="http://foo.com">
<meta name="twitter:card" content="summary">

<!-- 画像を載せたい場合 -->
<meta property="og:image" content="http://foo.com/bar.jpg">
```

## ポイント

* 画像は本番環境の絶対パスである必要があります。
