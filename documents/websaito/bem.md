# BEM

## 概要

{% embed data="{\"url\":\"https://www.youtube.com/watch?time\_continue=760&v=Put2HqjL2wg\",\"type\":\"video\",\"title\":\"BEM\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/Put2HqjL2wg/maxresdefault.jpg\",\"width\":1280,\"height\":720,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/Put2HqjL2wg?rel=0&showinfo=0&start=760\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/Put2HqjL2wg?rel=0&amp;showinfo=0&amp;start=760\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778}}" %}

CSSを設計する際、クラス名やスタイル指定のルールがないと、複数人でWebサイトを制作する際に統制が取れなくなります。BEMは最もポピュラーなCSS設計の手法で、Webサイトを構成するコンポーネント（パーツ）単位でCSS設計を行います。BEMで覚えるべき記法は以下の3つだけです。

```
.block
.block__element
.block--modifier
```

`.block` はコンポーネントを指します。`.block__element` はblockに依存する子要素を指します。 `.block--modifier` はblockの装飾を指します。このようにblockに紐づけてclass命名を行うことで、elementがblockの構成要員であることを明示的に示すことができます。

単語区切りは `-` で表現します。単語区切りを区別をつけるためにBEM記法では modifier が `--` 、 element が `__` であることに注意してください。

### 注意点

* .element は子供を持ちません。したがって `.block__element__element` のようなCSS命名はNGです。
* modifier はblockに対するものです。したがって `.block--modifire--modifire` はNGです。
* modifier はblock に対するものです。したがってmodifier単体でclass名が存在することはあり得ません。 `<div class="btn--red">` はありえません。 \`&lt;div class="btn btn--red"&gt;\` が正です。

### 公式ドキュメント

{% embed data="{\"url\":\"http://getbem.com/\",\"type\":\"link\",\"title\":\"BEM — Block Element Modifier\",\"description\":\"BEM — Block Element Modifier is a methodology, that helps you to achieve reusable components and code sharing in the front-end.\",\"icon\":{\"type\":\"icon\",\"url\":\"http://getbem.com/assets/favicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"http://getbem.com/assets/bem\_black.png\",\"width\":400,\"height\":400,\"aspectRatio\":1},\"caption\":\"厳密には公式サイトは存在しない\"}" %}

## Example

{% embed data="{\"url\":\"https://codepen.io/deerboy/pen/yKQdXj\",\"type\":\"rich\",\"title\":\"yKQdXj\",\"description\":\"...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://codepen.io/favicons/favicon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://s3-us-west-2.amazonaws.com/i.cdpn.io/355059.yKQdXj.small.870aa25c-240e-470f-b7df-54e460c9e090.png\",\"width\":384,\"height\":225,\"aspectRatio\":0.5859375},\"embed\":{\"type\":\"app\",\"url\":\"https://codepen.io/deerboy/embed/preview/yKQdXj?height=300&slug-hash=yKQdXj&default-tabs=css,result&host=https://codepen.io&embed-version=2\",\"html\":\"<iframe src=\\\"https://codepen.io/deerboy/embed/preview/yKQdXj?height=300&amp;slug-hash=yKQdXj&amp;default-tabs=css,result&amp;host=https://codepen.io&amp;embed-version=2\\\" style=\\\"border: 0; width: 100%; height: 300px;\\\" allowfullscreen></iframe>\",\"height\":300,\"aspectRatio\":null},\"caption\":\"BEM 使用例\"}" %}



