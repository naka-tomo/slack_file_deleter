# slack_file_deleter

Slackにアップロードした古いファイルを削除するプログラム

## 使用方法
1. `token`に[slack apiのページ](https://api.slack.com/apps)で作成したtokenを代入して実行
2. そのまま実行すると削除されるファイル名が表示されるので確認
3. 確認ができたら以下の箇所のコメントを外してもう一度実行し，ファイルを削除
  ```
    # 実際に削除する場合は以下のコメントアウトを取る
    #ret = delete_file( id )
    #print( ret )
  ```

## Tokenの作成方法
1. slackにログインし[このページ](https://api.slack.com/apps)で[Create New App]を選択
2. 適当なApp Nameをつけて，ファイルを削除したいワークスペースを選択して[Create App]
3. 左側のメニューから「OAuth & Permissions」を選択
4. User Token Scopes内にあるAdd an OAuth Scopeボタンで以下の２つを追加
  - files:read
  - files:write
5. 上の方にあるInstall App to Workspaceボタンを押して，Appをインストール
6. OAuth Access Tokenというところに表示されている文字列がトークンです．
