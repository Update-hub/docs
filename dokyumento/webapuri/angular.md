# angular

### 公式ドキュメント

{% embed data="{\"url\":\"https://angular-ja.firebaseapp.com/\",\"type\":\"link\",\"title\":\"Angular Docs\",\"icon\":{\"type\":\"icon\",\"url\":\"https://angular-ja.firebaseapp.com/assets/images/favicons/favicon-194x194.png\",\"width\":194,\"height\":194,\"aspectRatio\":1}}" %}

### Tips

#### 変更後のElementにStyleを適用させたい場合

{% code-tabs %}
{% code-tabs-item title="style.scss" %}
```css
:host ::ng-deep {
    ...
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="warning" %}
この方法は公式で非推奨だが現状代替案がないためしょうがない\(2018/4/7\)
{% endhint %}



