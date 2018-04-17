# stage-2:開発トレーニング

## 概要

このステージでは実務を想定したチーム開発を行います。この結果はUpdateサイトの実績一覧に掲載され、さらに各メンバーの実績にもなるため、ポートフォリオとして見られることを意識して取り組みましょう。

### 参加条件

期限のあるチームプレーとなるため、以下の条件を満たせない方はこのステージに参加できません。

* 不規則な生活リズムの方（特別な事情を除く。バイトの都合で毎日夕方から数時間など決まっていればOK。いつどれくらい稼働するのかまったく読めないのはNG）
* 週2日以下の稼働しかできない方

### 事前準備

* [PugLintの導入](https://docs.update.jp/document/websaito/pug#puglint)

### ルール

リモートにおけるチーム開発では毎日顔を合わせず、互いの稼動タイミングもバラバラなので、各メンバーがいつどれくらい動けるかを全員で把握する必要があります。そのためチーム開発中は以下のルールを守ってください。

* 「作業の開始」「作業の終了&進捗共有」を稼働日に必ずチームチャンネルで報告する。
* 個人の都合で稼働予定日に稼働できない場合、事前に連絡する。
* チームメンバーへの連携を忘れない。（共有、感謝、協力、相談）

{% hint style="danger" %}
無断で稼動しないのはチームに迷惑をかけるのでNG。
{% endhint %}

職業訓練も兼ねているため、単なるトレーニングではなく「チームでの仕事」だという意識を持って緊張感を持って取り組みましょう。

## チュートリアル

{% page-ref page="../dokyumento/websaito/pug.md" %}

{% page-ref page="../dokyumento/ji-chu-zhi-shi/chmu.md" %}

## 課題

[https://classroom.github.com/a/esI7PLw7](https://classroom.github.com/a/esI7PLw7)

[issue一覧](https://github.com/Update-hub/stage-2/issues)

### リーダーによる環境構築

1. リーダーが課題リポジトリ作成後、メンバーをアサインしてください。
2. チーム用のslackチャンネルを作成し、開発メンバーを招待してください。
3. `/github subscribe <リポジトリURL or リポジトリパス> reviews comments branches` のコマンドを、slackの通知が欲しいチャンネルで入力してください。以後slackチャンネルにリポジトリの通知が来るようにしてください。
4. master リポジトリにプロテクトをかけてください



![&#x8A2D;&#x5B9A;&#x9805;&#x76EE;](../.gitbook/assets/sukurnshotto-2018-04-14-180826.png)

以上でリーダーの開発準備は完了です。次のフローに進みましょう。

### 全体フロー

1. 各メンバーの稼働予定を確認してください。\(毎週何曜日何時間ほど動けるのか？）
2. 稼働量、スキルに基づいて実現可能な開発期間と調整マイルストーンをそれぞれ作成してください。
3. チームで相談し、各自issueを割り振ってください。\(asigneesにuserを設定, マイルストーンにクライアントチェックを設定\)
4. クライアントチェック日、リリース予定日をクライアントに報告してください。
5. issueの期限に沿って各自を開発をはじめてください。
6. 「作業の開始」「作業の終了&進捗共有」を稼働日に必ずチームチャンネルで行ってください。可能であればチームで時間を揃えてください。（例: 夕方17:00に進捗共有など）
7. クライアントチェックの日になったらGitHub Pages にデプロイした状態でクライアントに報告してください。
8. クライアントのFBと細かな調整、検品が終わったら実績ページにリリースされ、終了となります。

### 補足

* マイルストーンとは期間のことです。通常リリースまでには「開発期間」「クライアントチェック」「クライアントのFB対応、調整期間」が最低限必要になります。
* リリースの前には必ずクライアントチェックが挟まります。「この状態で公開して良いのか？」を確認する。通常この時点でいくつか修正が入りますので、最終調整フェーズは2、3日あると良いでしょう。

## ポイント

* 平日日中\(10:00 - 19:00\)稼働週末休みなど、実際の仕事と合わせることを推奨します。
* 与えられたissueが間に合いそうにない場合、間に合いそうにない旨をメンバーに共有し、issue配分を調整してもらう。（事前に連絡がなく期限を過ぎるのはNG）
* 仕様の不明点はクライアントに、技術的な不明点はチームメンバーに相談する。
* よくわからないまま進めない。
* 予定はキツキツで立てず、バッファ（余裕）を持たせる。キツキツで立てるとイレギュラー発生時に対応できなくなり、過度な残業につながる。
* リリース予定日を守る
* リーダー はあくまで進行管理役、クライアントとの折衝役であり、メンバーとの間に上下関係はありません。
* 担当以外のコードもコードレビューを通して確認し、理解を深める。
* クライアントチェック日当時になってクライアントに「できていません。」というのはNG。日々の進捗共有の中で厳しいと分かった時点でクライアントにチェック日の変更を打診する。

## 課題終了後

この課題が終わったら未経験のレイヤーでいうと非常に高いスキルを有する状態になります。具体的には以下のことができるようになっています。

* pugの利用
* gulpの利用
* sassの利用
* BEMによるコンポーネント設計
* モバイルファーストでのコンポーネント設計
* HTML Validatorに対応するマークアップ
* カルーセル、メニュー開閉など頻出コンポーネントのJS, jQuery実装
* Gitによるソースコード管理
* GitHub Flow によるコード管理（レビューし、masterにマージする体制）
* GitHubでのプロジェクト管理
* ピクセルパーフェクトでのコーディング（デザインに1px単位で準拠すること）
* グリッドレイアウトでのサイト設計

今回のリポジトリ、公開URLはそのまま自分のポートフォリオ、及び就職活動に実績に使っていただくことができます。その際、自分の担当範囲以外のパートについても説明できるよう、チームメンバーのソースコードを参考に知見を深めましょう。

### 今後のアクション

* より成長したい方はこのまま Stage-3 の上級トレーニングに進んでください。
* 現時点のスキルで就業したい方は前述したスキルセットとリポジトリを武器に就業活動をはじめてください。
* Update Workで仕事を探す場合、プロテストに進んでください。


