# conversation-noderedflow

Node-REDでConversationサービスを使ったアプリを作成する手順を紹介します。

## ファイル一覧
・手順書
　>README.md

・Node-REDフロー
　>conversation-nodered-flow.txt

・Conversationフロー
　>workspace-music.json


## アプリの作成手順
1. Bluemix上で、「Node-RED Starter」を作成します。
2. 作成したら、Node-REDの実行環境に、「Conversation」サービスをバインドし、Node-REDアプリを再ステージングします。
3. Node-REDアプリが「実行中」となったら、「Visit your App」からアプリを開きます。
4. Node-REDフローを開いたら、Node-REDフローをインポートします。  
インポートの手順は、右上の「読み込み」→「クリップボード」に、conversation-nodered-flow.txtを全コピーし、貼り付けます。
5. 「1.学習・データ登録」フローで、workspaceを作成し、workspace_idをメモする。
6. 「デバッグ」フローの「conversation」ノードに先ほどメモしたworkspace_idを入力する。  
「こんにちは」ノードをクリックし、debugタブに「こんにちは！今日の気分はどう？」と出力されることを確認する。
7. 「2.メイン」フローの「conversation」ノードに先ほどメモしたworkspace_idを入力する。  
ブラウザから、アプリのURLの末尾に「/conversation」を加えたURLを開き、会話ができることを確認する。

	入力、出力の例
	【入力		→【出力】
	①こんにちは	→こんにちは！今日の気分はどう？
	②悲しい		→では、悲しいときに元気が出る曲を<a href="https://www.youtube.com/watch?v=aaOpAo4UtAg" target="_blank">こちら</a>から流します！
	③音楽をききたい	→どんな音楽がいい？
	④今日雨ふる？	→今日の天気は晴れ！最高気温24度。かなり温かい1日です。


## conversationの会話フローの入力・出力
①【入力】おはよう→【出力】今日はよく眠れた？ →【入力】はい/いいえ→【出力】

②【入力】音楽をききたい→【出力】どんな音楽がいい？→【入力】ロック/クラシック/JPOP/ヒップホップ/トップ10→【出力】

③【入力】音楽をとめて→【出力】音楽を停止するね。 

④【入力】今日雨ふる？→【出力】今日の天気は晴れ！最高気温24度。かなり温かい1日です。

⑤【入力】悲しい/嬉しい/楽しい/不安→【出力】

## 補足資料
また、別のConversationフローを作成する場合は、下記URLからダウンロードしてください。

https://www.ibm.com/developerworks/community/files/app#/file/eeda8d43-5590-446a-8353-cfb5eef3cdd8
