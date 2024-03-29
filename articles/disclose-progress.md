---
title: "進捗を晒すためにやっていること"
emoji: "🦔"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: ["リモートワーク", "コミュニケーション"]
published: true
---

こんにちは。
今回は積極的に進捗を晒していこうというお話です。

筆者が業務を行う上で心がけていることをここでも晒してみようと思います。

# まとめ

- 非同期的な進捗晒しに焦点を当てている
- 晒す方法
  - プロジェクト管理ツールに雑に投げる
  - キリが悪くてもプルリクエストを作る

# 前提

この記事の内容には次のような前提があります。

##### 普段の業務はフルコミットでない

筆者が学生をしながら業務を行っていることもあり、フルコミットはしていません。
つまり、1日のうちに業務に割ける時間がフルコミットに比べ限られているということです。

##### 非同期コミュニケーションが中心

リモートワークのため、基本的にはSlack等を使った非同期的なコミュニケーションが多いです。
お互いの手元が見えないため、進捗の可視化が難しいという課題感を感じていたりします。

# 進捗を晒すとは

意味はそのままですが、今回は「自分の作業の進み具合を関係者に共有すること」と定義します。
定例ミーティングでの進捗確認や、テキストベースでの非同期的な進捗共有などさまざまな形がありますが、今回は後者に焦点を当てています。

# 進捗の晒し方

## プロジェクト管理ツールに雑に投げる

筆者が携わるプロジェクトでは、GitHub ProjectsやZenHub、Backlogなどのプロジェクト管理ツールを使ってタスクの洗い出しや整理、担当者の決定を行う事が多いです。

このプロジェクト管理ツールに進捗を投げてしまいましょう。

たとえば、以下のようなケースを想定します。

1. 自分があるタスクにアサインされている
2. そのタスクは（サードパーティ製ライブラリを使う必要があるなどの）不確定要素が多いタスクである
3. そのタスクでは技術調査を含む実装まで行う

この場合、みなさんならどのように進めていくでしょうか？

技術的な調査を進めていくと、使用するライブラリの候補や各ライブラリのメリット・デメリット、最終的な決定など様々なアップデートがあります。
筆者はこれを逐次Issueに投げてしまいます。

![](/images/disclose-progress/screenshot.png)
*Issueにコメントを投げている例（内容は適当です）*

こうすることで、自分以外のメンバーにタスクの進行状況が晒され、「あ、わたぽんの技術調査進んでるな」と把握できるようになります。 また、細かくアップデートを投げることで、方針に間違いがあった際に、メンバーからより早く訂正してもらえるといったメリットもあります。
Slackなどのコミュニケーションツールと連携しておくと、更新通知も飛ぶので、おすすめです。

## キリが悪くてもプルリクエストを作る

プルリクエストはどのタイミングで作るのがベストでしょうか。おそらく、実装やコミットの整理が完了したタイミングでしょう。
しかし、常にキリのいいタイミングでプルリクエストを作れるとは限らず、中途半端な実装で1日の業務が終わってしまうケースが多々あります。
この場合はどうしましょうかしら。

私の中にある1つの考え方として「コミットなしは進捗なし」というものがあります。
これは、**いくらローカルで作業をしていたとしても、それを他の誰かが観測できなければ作業していないと同意と見做せる**ということです。
少し過激かもしれませんが、リモートワークかつ非同期コミュニケーション中心のプロジェクトでは、進捗を晒すことを筆者はそのくらい大事にしています。

少し話を戻すと、、、

「中途半端な実装で1日の業務が終わってしまった」

この場合、筆者は**どんなにキリが悪くても**その日の終わりにプルリクエストを作ります。 プルリクエストを作ってしまえば、差分を可視化でき、自分の状況を晒すことができます。
作業途中であることがわかるよう、Draftにしておくか、タイトルにwipなどのラベルを入れておきましょう。
これもプロジェクト管理ツール同様にSlack連携等しておくと通知が飛ぶのでおすすめです。

https://github.com/integrations/slack

# あとがき

筆者が普段の業務で心がけている進捗の晒し方を晒してみました。
この記事で「もっと進捗晒してこう！」と思える人が増える機会を作れたのなら本望です。

もし記事に間違いなどがあれば、コメント等で教えていただけると幸いです。
ご一読いただきありがとうございました！
