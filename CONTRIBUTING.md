# Contribution Guide
このノートへのコントリビュートガイドです．

## Issues
このノートに関するご指摘やご質問，ご提案はGitHub上で受け付けています．GitHubリポジトリのIssueとしてあなたの疑問を報告したり，アイデアを提案できます．
- ノートの内容に関する質問やご指摘 => [こちら]()から
- ノートのバグや問題の報告 => [こちら]()から
- 既存の内容に関する提案 => [こちら]()から
- 新しいトピックなどの提案 => [こちら]()から ※下記セクション「Features coming soon」も参照してください．
- その他のIssue => [こちら]()から

### Features coming soon
このノートには今後，以下のような機能を追加する予定です．それぞれに関する報告や提案は専用のIssueから行うことができます．
- 演習課題の追加 => ご指摘や提案は[こちら]()から
- MATLAB Graderへの対応 => ご指摘や提案は[こちら]()から

## Pull Request
ご自身の修正をノートに反映させるためにはPull Requestを行ってください．Pull Requestはいつでも歓迎しています．次の種類のPull Requestを受け付けています。
- 誤字脱字の修正
- サンプルコードの修正
- 別の説明方法の提案や修正
- 文章をわかりやすくするように改善

そのほか「このような修正/改善はどうでしょう？」という提案がある場合は、Issueを立てて相談してください．
基本的なPull Request（特に細かいもの）は、Issueを立てずにPull Requestを送ってもらって問題ありません．

### Pull Requestの送り方
Pull Requestは以下のステップで行うことができます．
1. Fork it ( http://github.com/username/projectname/forks )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create new Pull Request

Pull Requestについては以下のサイトを参照してください．
[初心者向けGithubへのPullRequest方法＠Qiita]( https://qiita.com/samurairunner/items/7442521bce2d6ac9330b)

### Contribution
Pull Requestを受け入れるとあなたの貢献がContributorsリストに追加されます．また，Pull Requestを送った内容はこのノートのライセンス（Apache 2.0 and CC BY-NC）が適応されます．これは，あなたの貢献がこのノートへの努力的な寄付となることを意味しています。

## ディレクトリ構造
プロジェクトのルートディレクトリ```pca_notes_matlab```の直下に現行の開発ディレクトリ```current```および過去バージョンのディレクトリ```drafts_20190409```などを置いています．開発および修正は```current```ディレクトリ内のファイルに対して行ってください．開発を進めていく途中で，ディレクトリ構造を大幅に変更する必要があると判断した場合にのみ，該当する```current```ディレクトリを過去バージョンとして保存し，新たに```current```ディレクトリを作成します．
```current```ディレクトリの直下には，```htmls```，```livescripts```，```src```というサブディレクトリを用意しています．```htmls```および```livescripts```にはそれぞれ，HTML版ノート，MATLABライブスクリプト版ノートが保存されています．ノートは章ごとに名付けられ保存されています．また，```src```ディレクトリは自作関数の保存場所として利用してください．
ディレクトリ構造の変更や修正についてもIssueでご提案ください．

## コミットメッセージ規約
この規約は下記より転用・一部改変して記載しています．
https://github.com/asciidwango/js-primer/blob/master/CONTRIBUTING.md

### コミットメッセージの構成
コミットメッセージは以下のような構成で書いてください．
- 1行目に概要
- 2行目は空改行
- 3行目から本文
- 最後に関連するIssue(任意)を書きます。

### コミットメッセージの具体例
以下にコミットメッセージの例を以下に示します．
``` EXAMPLE:
feat(ngInclude): add template url parameter to events

The `src` (i.e. the url of the template to load) is now provided to the
`$includeContentRequested`, `$includeContentLoaded` and `$includeContentError`
events.

Closes #8453
Closes #8454
```

### コミットメッセージ概要欄の詳細
コミットメッセージの概要欄はコミットタイプ，スコープ，コミットタイトルから成ります．

```
                         scope        commit title

        commit type       /                /      
                \        |                |
                 feat(ngInclude): add template url parameter to events

        body ->  The 'src` (i.e. the url of the template to load) is now provided to the
                 `$includeContentRequested`, `$includeContentLoaded` and `$includeContentError`
                 events.

 referenced  ->  Closes #8453
 issues          Closes #8454
```

### コミットタイプ
1行目はコミットタイプから書き始めます．コミットタイプには以下のものがあります．
- feat
    - 新しい機能（演習課題の追加やMATLAB Graderへの対応を含む）、章、節の追加など
    - 更新履歴に載るような新しいページを追加
- fix
    - 意味が変わる修正（間違いの修正など）
    - 更新履歴に載るような修正
- docs
    - README.mdやCONTRIBUTING.mdや本体のプロジェクト全体のドキュメントについて
- refactor
    - 意味が変わらない修正（不明瞭な記述の修正など）
    - 更新履歴に載らないような修正
- style
    - 章立ての間違いの修正やスペースやインデントの調整
- perf
    - パフォーマンス改善．警告文への対応．
- chore
    - その他
    - typoの修正など

コミットタイプは、迷ったらとりあえずchoreと書きます．scopeも省略して問題ないので以下のような形でも問題ありません。

```
chore: コミットメッセージ
```