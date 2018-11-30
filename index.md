![showKs logo](./images/showKs_logo.png)

# showKsとは

## 趣旨

日本最大級のコンテナ関連技術カンファレンスである[JapanContainerDays](http://containerdays.jp/)（通称”JKD”）。そこにはコンテナ技術に興味がある、あるいはコンテナ技術を愛している、ひょっとするとコンテナ技術ってよく分からない・・・なんて人も含め、本当に様々な人がたくさん集まります。

　「こんなに面白い人達が集まるなら、なにか面白いデモができるのでは？」
 
JKDのスタッフミーティングで出たそんな発言をきっかけにスペシャルチームが結成されました。業務でバリバリにコンテナを技術を使っている凄腕エンジニアから、コンテナ業界を盛り上げているコミュニティの運営者まで、様々な組織の枠組みを超えて結束したまさに”ドリームチーム”が誕生したのです。

　「kubernetes上で実際にアプリが動く環境を皆さんに見てもらいたい！」
　「クラウドネイティブな開発も体験して欲しい！」
　「参加者に持って帰って貰えるようなものにしよう！」
　「アプリに面白さも欲しいよね！」

そんな熱い想いを原動力に、連日深夜まで苦労すること数ヶ月、ついにクラウドネイティブな開発を誰にでもお手軽にお試しいただける、参加体験型の “showKs（ショーケース）” ができあがりました。

このドリームチームの最後の1ピースはあなたです。

是非、あなたもドリームチームに参加して、クラウドネイティブな開発を体験してください。

## showKs構成概要

showKsでは、お絵かきアプリ[showks-canvas](https://github.com/containerdaysjp/showks-canvas)を題材にクラウドネイティブな開発を体験して頂けます。

![architecture simple](./images/architecture_simple.png)

上図の流れは、おおよそ以下の通りです。

1. [登録フォーム](http://form.stg.showks.containerdays.jp/projects/new)からユーザ登録
2. あなた専用のGithubリポジトリが自動作成
3. コードを変更してcommit
4. staging環境へアプリコンテナが自動ビルド/デプロイ
5. ブラウザからCanvasアプリへアクセスし動作確認
6. stagingブランチからmasterブランチへPullRequest/merge
7. production環境へアプリコンテナが自動ビルド/デプロイ
8. ブラウザからCanvasアプリへアクセスし動作確認

[詳細な手順](#showKsへの参加方法)

# showKs Canvasアプリ

![showks-canvas](./images/showks-canvas.png)

## 特徴

## ポータルについて

![showks-canvas-portal](./images/showks-canvas.png)

## 制約

# showKsへの参加方法

showKsへの参加およびクラウドネイティブアプリケーション開発体験の手順は、[こちら](./howToJoin.md)をご参照ください。  

# ドキュメントリンク

[showKs-doc](https://github.com/containerdaysjp/showks-docs)


