# showKsとは

## 趣旨

## 仕組み

# showKs Canvasアプリ

## 特徴

## ポータルについて

## 制約

# showKsへの参加方法

[こちら](./howToJoin.md)

## 1. 事前準備

showKsの参加には[Github](https://github.com)のアカウントが必要です。必ず事前にGithubアカウントを作成し、ユーザ名を確認しておいてください。

## 2. ユーザ名の登録

まずshowKsへ参加するためのユーザ登録をします。

[Project一覧](http://form.stg.showks.containerdays.jp/projects/)ページにアクセスし、既存の`Username`を確認します。  

次に、画面下部の`Create Project`をクリックして[登録フォーム](http://form.stg.showks.containerdays.jp/projects/new)に進みます。　

[登録フォーム](http://form.stg.showks.containerdays.jp/projects/new)では、次の情報を入力します。

![Image]()

- Username（必須） 
    - showKsで使用するユーザ名です。
    - 既存のUsernameと重複しないようにしてください。
        - 重複した場合、既存データ等を上書きしますのでご注意ください。
    - このユーザ名を元にあなた専用のリポジトリが[Github](https://github.com/containerdaysjp)上に作成されます。
- Github（必須） 
    - あなたのGithubアカウント名を入力してください。
    - このアカウントはお絵かきアプリからLinkされます。
    - 存在しないGithubアカウント名が指定された場合はエラーになります。
- Twitter（必須） 
    - あなたのTwitterアカウント名を入力してください。
    - このアカウントはお絵かきアプリからLinkされます。
    - Twitterアカウントをお持ちでない場合は`containerdaysjp`を指定します。
- Comment
    - 任意のメッセージを入力します。
    - このメッセージはお絵かきアプリに表示されます。

入力後、 `Create Project` をクリックすることで新しいProjectが作成されます。作成完了までは暫く時間がかかります。画面が遷移し`Project was successfully create`の表示がでるまで待機してください。

## 3. あなた専用リポジトリの確認

ユーザ登録により、あなた専用のリポジトリが自動的に用意されます。
このリポジトリは、[showks-canvas](https://github.com/containerdaysjp/showks-canvas)からForkされたものです。

[Github](https://github.com/containerdaysjp)へアクセスし、あなた専用のリポジトリが作成されていることを確認します。リポジトリ名は`showks-canvas-ユーザ名`で作成されています。検索機能がありますので活用してください。

あなた専用のリポジトリには、次のブランチが用意されています。

- staging
    - staging（ステージング）環境用のブランチです。
    - 今回、stagingブランチには直接commitしてコードを更新します。
- master
    - production（本番）環境用のブランチです。
    - 直接commitはせずに、stagingブランチからPull-Requestを発行してコードをmergeします。


## 4. Staging環境のポータル画面にアクセス

[staging環境用のポータル画面](http://portal.stg.showks.containerdays.jp)にアクセスします。

このポータル画面では、staging環境にデプロイされたshowKs-canvasアプリコンテナからの情報が集約表示されます。

showKsで事前に準備されているパイプライン管理から、ユーザ登録を契機にあなたのアプリコンテナが自動的にビルド/デプロイされます。

デプロイまでは少々のお時間が必要になりますので、表示がされない場合は暫く時間を空けてから再確認してください。

デプロイされたshowKs-canvasアプリでは実際にお絵かきをすることが可能です。お絵かきした内容は一定時間を置いた後にポータル画面にも反映されますので、挙動を確認してみてください。

## 5. ソースコードの更新（stagingブランチ）

あなた専用のリポジトリ（`https://github.com/containerdaysjp/showks-canvas-ユーザ名`）にアクセスします。

次の画像を参考に、Branchを`master`から`staging`に切り替えます（直接`https://github.com/containerdaysjp/showks-canvas-ユーザ名/tree/staging`にアクセスしても構いません）。

![Image]()

stagingブランチに切り替わったら、ファイルブラウザから `srcフォルダ` > `data`フォルダ > `author.json` の順にクリックします（直接`https://github.com/containerdaysjp/showks-canvas-ユーザ名/blob/staging/src/data/author.json`にアクセスしても構いません）。

画面右側にある鉛筆マークをクリックし、`author.json`を直接編集します。

ユーザ登録の際に入力された値がjson形式で埋め込まれていますので、`comment`の値だけを任意の文字列に置き換えてください。

値を更新後、画面下部の`Commit changes`欄に適切なコメントを入力し、`Commit directly to the staging branch.`にチェックが入っていることを確認してから`Commit changes`ボタンをクリックします。

showKsで事前に準備されているパイプライン管理から、commitを契機にあなたのアプリコンテナが自動的に再度ビルド/デプロイされます。

**注意：`author.json`以外のファイルを更新した場合は制約違反として自動ビルドが中止されます。その他のファイルは更新しないようにご注意ください。**

[staging環境用のポータル画面](http://portal.stg.showks.containerdays.jp)にアクセスし、ご自分のshowKs-canvasアプリコンテナが新しいものに置き換わることを確認します。

デプロイまでは少々のお時間が必要になりますので、表示がされない場合は暫く時間を空けてから再確認してください。

今回のアプリケーション仕様から、再デプロイされたアプリコンテナでは以前のお絵かきデータが引き継がれません。キャンバスが白紙に戻ることも確認します。

# ドキュメントリンク

[showKs-doc](https://github.com/containerdaysjp/showks-docs)


