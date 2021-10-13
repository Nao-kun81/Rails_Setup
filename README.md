# tup Ruby on Rails(2021/10)

# 環境構築の全体の流れを紹介します。  
・Rubyのダウンロード  
・SQLite3のインストール  
・Bundlerのインストール  
・Node.jsのダウンロード  
・yarnのダウンロード  
・railsのインストール  
・webpackerのインストール  
・新規プロジェクトの作成  
・ローカルサーバの起動  

## 【Rubyのダウンロード】  
まずはRubyのダウンロードを行います。下記のRubyダウンロードサイトから最新版を選択してください。  
＞　https://rubyinstaller.org/downloads/  

Windowsが64bit版の方は(×64)を、32bit版の方は(×86)を選択してください。64bitか32bitかの確認方法は下記のサイトを参考にしてください。  
＞　https://faq.nec-lavie.jp/qasearch/1007/app/servlet/relatedqa?QID=018022  

ダウンロード後、コマンドプロンプト(cmd)が自動で起動されると思いますので表示される[数字]を入力(カンマ含む)、Enterを押してください。  
ダウンロードが完了したら[Enter]と表示されるのでEnterを押してください。するとコマンドプロンプトが終了します。  
再度コマンドプロンプトを起動して、「ruby -v」と入力して「v ◯◯◯」とバージョンが確認できたらRubyのダウンロードは完了です。  

## 【SQLite3のインストール】  
次にRailsの開発において必要なデータベースを担うSQLite3をインストールします。下記のサイトより以下のファイルを選択してください。  
＞　https://www.sqlite.org/download.html  

「sqlite-dll-win-×64-3360000.zip」(32bitは×86)  
「sqlite-tools-win32-x86-3360000.zip」  

２つのファイルがダウンロードできたらエクスプローラーより解凍を行ってください。解凍したフォルダにあるそれぞれのファイルをRubyのbinファイルにコピペしてください。  

「sqlite-dll-win-×64-3360000.zip」(32bitは×86) >> 「sqlite3.dll」 >> 「C:Ruby￥bin」にコピペ  
「sqlite-tools-win32-x86-3360000.zip」 >> 「sqlite3.exe」と「sqlite3_analyzer.exe」 >> 「C:Ruby￥bin」にコピペ  

そしたらコマンドプロンプトで「gem install sqlite3」を実行してSQLite3をインストールします。完了したら「sqlite3 --version」でバージョンが確認できたら完了です。  

## 【Bundlerのインストール】  
Bundelerのインストールは非常に簡単でコマンドプロンプトで下記のコマンドを実行してください。  
「gem install bundler」インストールが完了したら「bundler -v」でバージョンが確認できたら完了です。  

## 【Node.jsのダウンロード】  
Node.jsはサーバの構築などができるJavaScriptのライブラリです。下記のサイトよりLTS(推奨版)をダウンロードしましょう。  
＞　https://nodejs.org/ja/  

ダウンロードが完了するとPowerShellが起動すると思いますので[Enter]と表示されたらEnterを押して進めてください。  
ダウンロードが完了したら、コマンドプロンプトを起動して「nodejs -v」でバージョンが確認できたら完了です。  

## 【yarnのダウンロード】  
yarnのダウンロードはnpm経由で行うとバージョンを確認した際に非推奨との警告が出て、後のローカルサーバの起動でエラーが発生しますので下記のサイトよりinstallerをダウンロードしてください。  
＞　https://classic.yarnpkg.com/en/docs/install#windows-stable  

installerはこのサイトの[Alternatives]というところをクリックすると表示されますので、Operating system:WindowsでVersion:Classic Stableを選択して[Download Installer]をクリックしましょう。  
ダウンロードが完了したらコマンドプロンプトを起動して「yarn -v」でバージョンが確認できたら完了です。  

## 【railsのインストール】  
ようやくRailsのインストールを行っていきます。railsのインストールはコマンドプロンプトで下記のコマンドを実行してください。  
「gem install rails」人によっては数分くらいインストールに時間がかかるかもしれません。最後に「rails -v」でバージョンを確認できたら完了です。  

## 【webpackerのインストール】  
最後のインストール作業です。これもコマンドプロンプトで下記のコマンドを実行してください。  
「rails webpacker:install」これはすぐインストールできると思います。これはバージョンがないのでコマンドさえ実行できればokです。  

## 【新規プロジェクトの作成】  
それではrailsでプロジェクトを作成しましょう。コマンドプロンプトでプロジェクトを作成したディレクトリに移動して、「rails new プロジェクト名 -G」を実行してください。  
Gitをすでにダウンロードしている方は最後の「-G」は不要になります。  

## 【ローカルサーバの起動】  
作成したプロジェクトのディレクトリに移動して下記のコマンドを実行してください。  
「rails s」エラーが表示されなければお使いの検索エンジン(gooogleなど)のURL入力で「localhost:3000」と入力すると  
「Yay! You're on Rails!」と表示されると思います。  


これでRuby on Railsの環境構築は完了です。
