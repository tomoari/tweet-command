Tweet command
=============

## これはなに
名前のごとく

## インストールなど
以下のものが必要です:

* Linux / UNIX 的な環境 (Windowsでは多分動きません, 後ほど修正します)
* Ruby (1.9.3 での動作しか確認していませんが、1.8.7でも動くかもしれません)

実行時にスクリプトへのパスを毎回指定したい稀有な人間でないのならば、chmodで実行権をつけて /usr/local/bin などのパスが通っているディレクトリにスクリプトへのシンボリックリンクでも貼っておくと良いでしょう。

	~/tweet-command$ chmod 755 tweet.rb

	/usr/local/bin# ln -s ~/tweet-command/tweet.rb tweet

## 使い方
標準入力から読み込んだ文字列をTwitterにポストします。  
初回起動時は認証が必要なので、指示に従ってPINコードを入力してください。  
コマンドライン引数は*受け付けない*ので注意してください。

	echo 'Hello Twitter!' | tweet

## アカウントを変えたい
認証情報を $HOME/.tweet に保存しているので、そのファイルを消せば再認証できます。

## FAQ
* なんか失敗する : 多分バグです
* 失敗してるのに"succeeded"とかほざく : まあ妥当に考えてバグでしょう
* コードが汚い : 眠気の限界
