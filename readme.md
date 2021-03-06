# quiz.vim

![ScreenShot](http://gyazo.com/d09107a1f4ad2974f5f0e5c0bc627ac6.png)

vimでコーディング中にクイズで頭をリフレッシュできるプラグインです。

## 説明

vimでコーティング中に、ちょっとだけリフレッシュしたいと思ったことはありませんか？そういう時に何をしますか？「ニュース」「Twitter」「ジャグリング」「お茶」「環境設定」「ゲーム」でしょうか。他にも色々ありますね。どれもリフレッシュできると思います。そう、それともう一つありますね。頭の体操ができるスポーツ「クイズ」です。

今、あなたはvimでコーディング中です。

vimという環境から離れたくないとは思っているものの、離れて一息ついてしまうと長い時間になる事もあるのでは？そういう時にこのクイズプラグインが役に立ちます。

目の前のコードはそのままに、画面を切替えず操作をできるので「あれっ？続きはどこだったけ？」となりません。リフレッシュされた脳により作業効率があがる事でしょう。(あなたにとってクイズに使う最適な時間はあなたにしかわかりません)

クイズの問題は10万を超える問題を取り扱っている日本最大のクイズサイト「[クイズ研](http://quizken.jp/)」のサイトから[WebAPI](http://quizken.jp/api/ma6)を使って取得していますので、バリエーション豊かにリフレッシュタイムを過ごせると思います。

Enjoy Programing and Refresh Time.

## インストール

vimのruntimepathのpluginディレクトリにquiz.vimを配置します。
runtimepathは「set runtimepath?」で知ることができます。

### 依存ライブラリ

http通信にcurlを利用しています。

Windowsでvimを使っている方は[Kaoriyaで配布されているcurl](http://www.kaoriya.net/dist/curl-7.10.8-win32-ssl.tar.bz2)をダウンロードしパスを通しておきます。

Macでは標準でインストールされています。Linuxでインストールはyumやaptなどのパッケージ管理ソフトでインストールするといいでしょう。

## 使い方

コマンドラインモードで下記のコマンドを実行します。

    :Quiz

引数として数値を与えることにより問題数を指定することができます。

WebAPIの仕様により指定できる問題数は1問〜50問です。

    :Quiz 10

## 設定

.vimrcに下記設定を書くことで瞬時にクイズを実行することができます。

### デフォルト値

    let g:quiz_count = 5

:Quizを実行した時に何問出題するかを設定できます。

### キーマッピング

    noremap <space>qz :Quiz<enter>

ノーマルモードでスペースキー q z とタイプするとクイズが始まります。
