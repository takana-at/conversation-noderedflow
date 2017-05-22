# conversation-noderedflow

Node-REDでConversationサービスを使ったアプリを作成する手順を紹介します。

##ファイル一覧
・Node-REDフロー
　>conversation-nodered-flow.txt

・Conversationフロー
　>workspace-music.json


##アプリの作成手順
①Bluemix上で、「Node-RED Starter」を作成します。

②作成したら、Node-REDの実行環境に、「Conversation」サービスをバインドし、Node-REDアプリを再ステージングします。

③Node-REDアプリが「実行中」となったら、「Visit your App」からアプリを開きます。

④Node-REDフローを開いたら、Node-REDフローをインポートします。
　インポートの手順は、右上の「読み込み」→「クリップボード」に、conversation-nodered-flow.txtを全コピーし、貼り付けます。

⑤「1.学習・データ登録」フローで、workspaceを作成し、workspace_idをメモする。

⑥「デバッグ」フローの「conversation」ノードに先ほどメモしたworkspace_idを入力する。
「こんにちは」ノードをクリックし、debugタブに「こんにちは！今日の気分はどう？」と出力されることを確認する。

⑦「2.メイン」フローの「conversation」ノードに先ほどメモしたworkspace_idを入力する。
ブラウザから、アプリのURLの末尾に「/conversation」を加えたURLを開き、会話ができることを確認する。

	入力、出力の例【入力→【出力】
	
	①こんにちは→こんにちは！今日の気分はどう？
	
	②悲しい→では、悲しいときに元気が出る曲を<a href="https://www.youtube.com/watch?v=aaOpAo4UtAg" target="_blank">こちら</a>から流します！
	
	③音楽をききたい→どんな音楽がいい？
	
	④今日雨ふる？→今日の天気は晴れ！最高気温24度。かなり温かい1日です。
	
	
