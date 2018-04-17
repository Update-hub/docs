# チーム開発

## 概要

* Updateにおけるリーダーはあくまで進行管理役であり、上下関係はないのでフラットなチームビルディングを行いましょう。
* 高確率でだれてくるので、毎日or毎週決まった時間にメンバーで進捗共有を行いましょう。
* 稼動できない日、タイミングは前もってメンバーに共有しましょう。
* 誰がいつまでに何をやるかを明確にしましょう。
* 仕様上不明な点はクライアントに確認しましょう。想像で作業を進めるのは避けましょう。
* お互いに敬意を持って、丁寧に指示を出し、丁寧にお礼を言いましょう。

## クイックスタート

### 開発フロー

1. リーダーを決める（全体管理）
2. メンバーのリソースを確認する（誰がいつ、どれくらい稼動できるか）
3. 仕様を確認する
4. 仕様を作業単位でissueにする
5. メンバーのリソース、能力に応じてissueを割り振る
6. リリースから逆算して期限を設定する（必ずバッファを設ける）
7. 開発&ソースレビューを行う
8. クライアントチェックを行う
9. FB対応、最終調整を経て公開する

### ポイント

* リリースまでのスケジュールとタスク配分を見える化する。issue、milestone、スプレッドシートのガンドチャートなどを適宜利用。
* 週単位でチェックゲート（進捗がまずくないか確認するタイミング）を作り、スケジュールに間に合わないことが分かった時点でタスクの再配分やメンバーへの注意喚起、あるいはクライアントへのリリース時期調整要請を行う。

## トラブルシューティング

### 仕様に不明点がある

想像で勝手に進めるのは絶対にやめましょう。明らかに予測で対応できる場合を除き、基本的にはクライアントに正しい仕様を確認しましょう。作業開始前に仕様全体を精査し、不明点を事前に洗い出しましょう。

### 期限に間に合いそうにない

必ず事前にクライアント（トレーナー）に連絡しましょう。期限当日になってできていません。というのはプロとしては失格です。

### 問題のあるメンバーがいる

Updateにおいてはトレーナーに相談してください。実務においては上司に相談してください。稼働が明らかに少ないメンバーについては体調を崩さない範囲でプレッシャーを持って取り組むよう伝えましょう。
