![showKs logo](./images/showKs_logo.png)
  
   
# showKsとは ｜ 趣旨

日本最大級のコンテナ関連技術カンファレンスである[JapanContainerDays](http://containerdays.jp/)（通称”JKD”）。

そこにはコンテナ技術に興味がある、あるいはコンテナ技術を愛している、もしくはコンテナ技術ってなんだかよく分からない・・・などなど、様々な人達がたくさん集まります。

　「こんなにも面白い人達が集まるなら、なにか面白いデモができるのでは？」
 
JKDのスタッフミーティングで出てきたこんな発言をきっかけにスペシャルチームが結成されました。業務でバリバリにコンテナを技術を使っている凄腕エンジニアから、コンテナ業界を盛り上げているコミュニティの運営者まで、様々な組織の枠組みを超えて結束したまさに”ドリームチーム”が誕生したのです。

　「kubernetes上で実際にアプリが動く環境を皆さんに見てもらいたい！」  
　「クラウドネイティブな開発も体験して欲しい！」  
　「参加者に持って帰って貰えるようなものにしよう！」  
　「アプリに面白さも欲しいよね！」  

そんな熱い想いを原動力に連日深夜まで苦労すること数ヶ月、ついにクラウドネイティブな開発を誰にでもお手軽にお試しいただける参加体験型の “showKs（ショーケース）” ができあがりました。

このドリームチームに必要な最後の1ピースは**あなた**です。

是非、ドリームチームに参加してクラウドネイティブな開発を体験してください。  
  
  
# showKs構成

showKsでは、お絵かきアプリ[showks-canvas](https://github.com/containerdaysjp/showks-canvas)を題材にクラウドネイティブな開発を体験して頂けます。

JKD v18.12におけるshowKs環境は、[Kubernetes](https://kubernetes.io)のクラスターを[Google Cloud Platdform](https://cloud.google.com)上で構成し、[Concourse](https://concourse-ci.org)や[Spinnaker](https://www.spinnaker.io)などのCI/CDツールによりパイプライン管理をすることで、マイクロサービス化されたコンテナアプリをクラウドネイティブに開発できるように構成されています。

また、showksで使用しているコードや設定ファイル、ドキュメント等は[Github](https://github.com/containerdaysjp)上で公開されていますので、どなたでもご自分で同じ環境を作り上げることが可能です。

## showKsの参加および開発体験の流れ

![architecture simple](./images/architecture_simple.png)

1. 登録フォームからユーザ登録
2. あなた専用のGithubリポジトリが自動作成
3. コードを変更してfeatureブランチへcommit
4. featureブランチからstagingブランチへPullRequest/merge
5. staging環境へアプリコンテナが自動ビルド/デプロイ
6. ブラウザからCanvasアプリへアクセスし動作確認
7. stagingブランチからmasterブランチへPullRequest/merge
8. production環境へアプリコンテナが自動ビルド/デプロイ
9. ブラウザからCanvasアプリへアクセスし動作確認

詳細な手順はこちらの[参加手順](#showKsへの参加方法)をご確認ください。
  
  
## showKs Canvasアプリ

![showks-canvas](./images/showks-canvas-sample.png)

[Node.js](https://nodejs.org/)および[Socket.io](https://socket.io)を用いたお絵かきアプリです。[Socket.IO Collaborative Whiteboard](https://github.com/socketio/socket.io/tree/master/examples/whiteboard)をベースに作成されています。

このアプリケーションには次の機能が実装されています。

- Socket.io経由の複数ブラウザウィンドウ間におけるリアルタイム同期
- ユーザプロフィール（各アカウントおよびコメント）の表示
- 描写カラーの自由な選択
- スマホ/タブレット端末ブラウザからの描写
- 消しゴム機能

showKs Canvasアプリのリポジトリは[こちら](https://github.com/containerdaysjp/showks-canvas)です。showKsへの参加登録が完了すると、このリポジトリからForkされたあなた専用のリポジトリが自動的に作成されます。
  
  
## showKs portal

![showks-portal](./images/showks-portal-sample.png)

showKs参加者がそれぞれデプロイしたアプリコンテナから、ユーザプロフィールや画像データなどの情報を集約し、[Nuxt.js](https://nuxtjs.org)を利用して表示するのが"showKs portal"です。このポータル画面から各canvasアプリに移動してお絵かきをすることも可能です。

また、showKsにはstaging（ステージング）とproduction（本番）の2つの環境が用意されてますが、showKs portalは環境毎に独立して用意されています。

 - [staging環境用のポータル](http://portal.stg.showks.containerdays.jp)
 - [production環境用のポータル](http://portal.prod.showks.containerdays.jp)
  
  
# 注意事項

showKsの参加に際して、次の事項を遵守頂きますようご協力をお願いします。

- showKsで公開しているコードや情報などを無断で商用利用しないでください。
- Canvasアプリコンテナで公序良俗に反するコメントやイラストなどを表示させないでください。
  - Canvasアプリはインターネットへ公開される点にご留意ください。
  - [JKDのCode of Conduct（行動規範）](https://containerdays.jp/#event-slides)も併せてご一読ください。
  
  
# showKsへの参加方法

showKsへの参加手順は、[こちら](./howToJoin.md)をご参照ください。  
  
  
# ドキュメント

showKsで利用しているコンポーネントに関する情報は、次のドキュメントリポジトリに随時集約されます。

- [showKs-docs](https://github.com/containerdaysjp/showks-docs)
  
  
# 展示ブース

JKD v18.12では、受付隣の1番ブースにおいてshowKsのデモ展示をしています。

展示ブースでは次のようなConcourseやSpinnakerの管理者用ダッシュボードなどをご確認頂けます。

![showks-concourse](./images/showks-concourse.png)
![showks-spinnaker](./images/showks-spinnaker.png)

また、showKsに関しての質問も受け付けておりますので、なにかお聞きになりたいことがありましたらブース担当者までお気軽にお声がけください。

# セッション

JKD v18.12において、showKsに関するセッションを予定しています。showKsの舞台裏が気になる方は是非ご参加ください。

 - 日時：　2018/12/05 (水) 15:40 - 16:20
 - タイトル：　ユーザー参加型CI/CDの実験場「showKs」開発の舞台裏
 - 登壇：　太田 航平、草間 一人、吉瀬 淳一

# ハッシュタグ

showKsに関しては `#containerdaysjp`と `#showKs` の2つのハッシュタグをつけてのTweetにご協力をお願いします。
たくさんの感想やご意見をお待ちしております。

