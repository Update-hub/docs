# プロジェクトの進め方

## 概要

{% embed data="{\"url\":\"https://www.youtube.com/playlist?list=PLw1QAmLkyyagNWpS8ZhCeRcLP3Vfq\_hPa\",\"type\":\"video\",\"title\":\"トレーニングガイド\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/gBj\_PCqbydI/hqdefault.jpg\",\"width\":480,\"height\":360,\"aspectRatio\":0.75},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/videoseries?list=PLw1QAmLkyyagNWpS8ZhCeRcLP3Vfq\_hPa\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/videoseries?list=PLw1QAmLkyyagNWpS8ZhCeRcLP3Vfq\_hPa\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778}}" %}

プロジェクトを進める際の基本的なフローを説明します。

## ワークフロー

### 全体の流れ

大まかな流れです。各ステップの詳細は後述します。

1. GitLabプロジェクトの作成
2. GitHub Flowで課題に対応する
3. すべての課題が終わったら終了となる

### GitLabプロジェクトの作成

各プロジェクトのページにGitLabプロジェクトのzipが用意されています。所属チームのグループにzipをインポートする形でプロジェクトを作成します。インポートしたプロジェクトには課題や開発環境が内包されています。またチームのメンバーがアクセスできます。

#### インポートの方法

チーム開発プロジェクトの場合はリーダーのみが行ってください。他のメンバーはリーダーが作成したプロジェクトに対して作業を行なってください。

1. **所属チームのGitLabグループで**新規プロジェクトの作成をクリック
2. Import project のタブでGitLab export を選択し、プロジェクトのzipを選択する。プロジェクト名は「プロジェクト名-自分のgitlabId」としてください。
3. しばらくするとインポートが完了します。

#### Slackとの連携

プロジェクトをを作成したらプロジェクト設定&gt;integrations&gt;Slack notificationsと進み、各種チェック項目の値に自分のチーム名を入力してください。最後に、ページ下部の webhook の欄に下記のテキストを貼り付け、保存してください。

> https://hooks.slack.com/services/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

### 課題の対応

issue（課題）単位でブランチを作成します。ブランチ名は `feature/課題番号` としてください。対応が終わったらPushし、メンバーにマージリクエストを出してください。マージを待つか、あるいは並行して別issueのブランチを作成し、同様にマージリクエストを出して作業を進めてください。

### 課題の終了

すべての課題が正常に終了したら次のプロジェクトを開始します。

## Tips

### 分からない、つまづいた

プロジェクトに必要な知識はこのサイトに掲載してありますが、それでも分からない部分があった場合、自分で調べるかチームチャンネルでメンバーに聞いてください。メンバーが誰も分からない場合、\#ask チャンネルで聞いてください。

