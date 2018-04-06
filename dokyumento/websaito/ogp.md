# OGP

## 公式サイト

{% embed data="{\"url\":\"http://ogp.me\",\"type\":\"link\",\"title\":\"Open Graph protocol\",\"description\":\"The Open Graph protocol enables any web page to become a rich object in a social graph.\",\"icon\":{\"type\":\"icon\",\"url\":\"http://ogp.me/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"http://ogp.me/logo.png\",\"width\":300,\"height\":300,\"aspectRatio\":1}}" %}

## クイックスタート

OGPタグを設置するとSNSでURLをシェアした際、タイトルやサムネイルが表示されるようになります。

```markup
<meta property="og:title" content="OGPのタイトル">
<meta property="og:description" content="OGPのディスクリプション">
<meta property="og:url" content="http://foo.com">
<meta name="twitter:card" content="summary">

<!-- 画像を載せたい場合 -->
<meta property="og:image" content="http://foo.com/bar.jpg">
```

## Tips

* 画像は本番環境の絶対パスである必要があります。

