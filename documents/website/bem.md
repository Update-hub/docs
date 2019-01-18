---
description: 最もメジャーなCSS命名規則です。
---

# BEM

## 概要

{% embed url="https://www.youtube.com/watch?time\_continue=760&v=Put2HqjL2wg" %}

CSSを設計する際、クラス名やスタイル指定のルールがないと、複数人でWebサイトを制作する際に統制が取れなくなります。BEMはもっともポピュラーなCSS設計の手法で、Webサイトを構成するコンポーネント（パーツ）単位でCSS設計を行います。BEMで覚えるべき記法は以下の3つだけです。

```
.block
.block__element
.block--modifier
```

`.block` はコンポーネントを指します。`.block__element` はblockに依存する子要素を指します。 `.block--modifier` はblockの装飾を指します。このようにblockに紐づけてclass命名を行うことで、elementがblockの構成要員であることを明示的に示すことができます。

単語区切りは `-` で表現します。単語区切りを区別をつけるためにBEM記法ではmodifierが `--` 、elementが `__` であることに注意してください。

### 注意点

* .elementは子供を持ちません。したがって `.block__element__element` のようなCSS命名はNGです。
* modifierはblockに対するものです。したがって `.block--modifire--modifire` はNGです。
* modifierはblockに対するものです。したがってmodifier単体でclass名が存在することはあり得ません。 `<div class="btn--red">` はありえません。 \`&lt;div class="btn btn--red"&gt;\` が正です。

### 公式ドキュメント

{% embed url="http://getbem.com/" caption="厳密には公式サイトは存在しない" %}

## Example

{% embed url="https://codepen.io/deerboy/pen/yKQdXj" caption="BEM使用例" %}
