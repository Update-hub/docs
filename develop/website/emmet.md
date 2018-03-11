# Emmet

https://docs.emmet.io/

- Visual Studio Code をはじめとするモダンなエディタにははじめから内臓されています。

## BEM

BEMフィルターを使えばBEMの出力も可能。

```html
.hero>-msg|bem
```

とすることで下記のHTMLマークアップが行えます。

```html
<div class="hero">
  <div class="hero__msg"></div>
</div>
```