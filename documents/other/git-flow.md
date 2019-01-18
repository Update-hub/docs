# Git Flow

## 概要

もっともメジャーなブランチ管理手法です。採用条件に含まれることもあります。複雑ですが、SourceTreeなどのGitクライアントを使うことで直感的に操作が可能です。作業単位でfeatureブランチ、リリース単位でreleaseブランチ、バグ単位でhotfixブランチをそれぞれ作成し、developやmasterにマージする手法です。

[https://danielkummer.github.io/git-flow-cheatsheet/index.ja\_JP.html](https://danielkummer.github.io/git-flow-cheatsheet/index.ja_JP.html) [https://github.com/nvie/gitflow](https://github.com/nvie/gitflow)

## 使い方

Source Treeを使うと直感的にGit Flowで管理ができます。issue単位でfeatureを開始\(feature/issue番号\)し、作業が終わったらPushしてDevelopにMerge Requestを出します。マージされたら新しいfeatureを開始し、再度Merge Requestを出します。最終的に公開する時、releaseを行います。

{% embed url="https://qiita.com/\_rema\_lp/items/1758fa72221fb973f2c6" %}