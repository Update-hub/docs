---
description: 最もメジャーなCSS命名規則です。
---

# BEM

## 概要

{% embed url="https://www.youtube.com/watch?time\_continue=760&v=Put2HqjL2wg" %}

CSSを設計する際、クラス名やスタイル指定のルールがないと、複数人でWebサイトを制作する際に統制が取れなくなります。BEMはもっともポピュラーなCSS設計の手法で、Webサイトを構成するコンポーネント（パーツ）単位でCSS設計を行います。BEMの記法は以下の4つだけです。これ以外の組み合わせはありえません。(`div`である必要はないです)

```html
<div class="block（親）" />
<div class="block__element（親に必要なパーツ）" />
<div class="block block--modifier（親に対する装飾）" />
<div class="block__element block__element--modifier（パーツに対する装飾）" />
```

* `block` は再利用可能なコンポーネントです。
* `block__element` はblockに必要なパーツです
* `block--modifier` はblockやelemnetの装飾です

単語区切りは `-` で表現します。単語区切りを区別をつけるためにBEM記法ではmodifierが `--` 、elementが `__` であることに注意してください。

## 例

{% embed url="https://codepen.io/deerboy/pen/yKQdXj" caption="BEM使用例" %}

### 注意点

* .elementは子供を持ちません。したがって `.block__element__element` のようなCSS命名はNGです。
* modifierはblock、elementに対するものです。したがって `.block--modifire--modifire` はNGです。
* modifierはblock、elementに対するものです。したがってmodifier単体でclass名が存在することはあり得ません。 `<div class="btn--red">` はありえません。 \`&lt;div class="btn btn--red"&gt;\` が正です。

### 公式ドキュメント

{% embed url="http://getbem.com/" caption="厳密には公式サイトは存在しない" %}
