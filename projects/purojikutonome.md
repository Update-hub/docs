# プロジェクトの進め方

## 概要

プロジェクトを進める際の基本的なフローを説明します。

## ワークフロー

### 全体の流れ

大まかな流れです。各ステップの詳細は後述します。

1. GitLabプロジェクトの作成
2. Git Flowで課題に対応する
3. すべての課題が終わったら終了となる

### GitLabプロジェクトの作成

各プロジェクトのページにGitLabプロジェクトのzipが用意されています。所属チームのグループにzipをインポートする形でプロジェクトを作成します。インポートしたプロジェクトには課題や開発環境が内包されています。またチームのメンバーがアクセスできます。

#### インポートの方法

チーム開発プロジェクトの場合はリーダーのみが行ってください。他のメンバーはリーダーが作成したプロジェクトに対して作業を行なってください。

1. GitLabグループで新規プロジェクトの作成をクリック
2. Import project のタブでGitLab export を選択し、プロジェクトのzipを選択する。プロジェクト名は「プロジェクト名-自分のgitlabId」としてください。
3. しばらくするとインポートが完了します。

### Git Flow で課題に対応する

Source Tree を使うと直感的に Git Flow で管理ができます。issue単位でfeatureを開始\(feature/issue番号\)し、作業が終わったらPushしてDevelopにMerge Request を出します。マージされたら新しいfeatureを開始し、再度Merge Request を出します。最終的に公開する時、releaseを行います。

{% embed data="{\"url\":\"https://qiita.com/\_rema\_lp/items/1758fa72221fb973f2c6\",\"type\":\"link\",\"title\":\"Sourcetreeを使って既存のリポジトリをgit-flowにする - Qiita\",\"description\":\"\#\# git-flowを初期化する メニューバーより \[リポジトリ\] > \[Git flow / Hg flow\] > \[リポジトリの初期化\] をクリック !\[スクリーンショット 2018-02-25 16.06.17.png\]\(ht...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn.qiita.com/assets/favicons/public/apple-touch-icon-f9a6afad761ec2306e10db2736187c8b.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.qiita.com/assets/qiita-fb-2887e7b4aad86fd8c25cea84846f2236.png\",\"width\":200,\"height\":200,\"aspectRatio\":1}}" %}

### 課題の終了

すべての課題が正常に終了したら次のプロジェクトを開始します。

## Tips

### 分からない、つまづいた

プロジェクトに必要な知識はこのサイトに掲載してありますが、それでも分からない部分があった場合、自分で調べるかチームチャンネルでメンバーに聞いてください。メンバーが誰も分からない場合、\#ask チャンネルで聞いてください。

