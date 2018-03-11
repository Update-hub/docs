# Website

TODO: 動画載せる

最高品質のWebサイトを制作するためのTipsをまとめています。ここでまとめる内容は最先端かつ最高品質のものなので、このドキュメントにしたがってWebサイトを制作することができればプロのWebコーダーとして十分なレベルであると言えます。

### ピクセルパーフェクト

デザインをコーディングで実装する際、デザインに対し1pxのずれも許容しない精度をピクセルパーフェクトと呼びます。字間、行間、余白、線の太さ、色、すべてにおいてデザインを完全に再現することがプロの実装者に求められます。

PhotoShopやAdobe XD、Sketchが主に使われるデザインツール（いずれも有料）ですが、いずれにおいてもデザインの各種データ（文字サイズ、色）を制作に抽出する機能が備わっているため、デザインツールの基本操作も並行して身につけましょう。

デザインツールを持っていない方はデザイナーに各要素の数値データを提供してもらいましょう。フリーランスで生計を立てる場合、デザインの数値が取れないと仕事にならないため、いずれかのデザインツールは必ず購入しましょう。

## 検品

作成したサイトはクライアントチェックや公開前に必ず検品を行います。表示、動作上の不具合はもちろんコードの不備も徹底的に洗い出し、最高の品質に仕上げます。

### ツールチェック

| ツール | 概要 | 合格基準 |
| --- | --- | --- |
| [HTML Validator](https://validator.w3.org/) | HTML品質チェック | エラーがない状態にする\(外部ソースは除く\) |
| [構造化データテストツール](https://search.google.com/structured-data/testing-tool) | SEO対策 | エラーがない状態 |
| [Page Speed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=ja) | パフォーマンス改善 | PC, SPともにレッドスコアでないこと |
| [モバイルフレンドリー](https://search.google.com/search-console/mobile-friendly?hl=ja) | スマホ対応 | エラーがない状態 |
| [シェアデバッカー](https://developers.facebook.com/tools/debug/) | SNSシェア時にサムネイルなど表示するタグ | エラーがない状態 |
| [AMPテスト](https://search.google.com/test/amp) | AMPの場合 | エラーがないこと |
| [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk) | PWAの場合 | エラーがないこと |
| [Test My Site](https://testmysite.withgoogle.com/intl/ja-jp) | 表示速度と同業比較 | 要改善でないこと |

### ブラウザチェック

要件定義に基づき、各種ブラウザで表示や動作上の不具合がないか目視で確認しましょう。要件定義がない場合、モダンブラウザ（各端末の最新ブラウザ）で確認を行いましょう。デザインがある案件の場合、ピクセルパーフェクトの確認も欠かさず行いましょう。

* Chrome
* Safari
* Microsoft Edge\(旧IE\)
* Firefox
* Safari\(iOS\)
* Chrome\(Android\)

ブラウザの開発者ツールでスマートフォン、タブレットの表示をシュミレートすることができますが、特にタップ操作を伴うUIがある場合などは必ず実機で表示して確認を行いましょう。

#### 参考

* [ブラウザ別シェア](https://lab.syncer.jp/Statistic/Browser/2017/10/)
* [iOSシェア](https://developer.apple.com/support/app-store/)
* [Androidシェア](https://developer.android.com/about/dashboards/index.html)

### その他見落としがちなチェック項目

* favicon, スマホhome画面用アイコンは設置されているか
* titleは正しく設定されているか
* Sitemapは設置されているか



