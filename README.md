# HoloLensでJoyConを使えるように設定したInputManager

JoyCon(L)(R)を接続するとUnityがそれぞれJoypad1とJoypad2として認識する。  
LとRのどちらがJoypad1でどちらがJoypad2なのかは場合によってそれぞれだった。  
接続順によるのかもしれないが未確認。  

UnityのInputManager設定で、Joypad1のbutton 0がAボタンというように、  
すべてのボタンとスティックについて入力を割り当てることで、  
(L)(R)の入力をそれぞれ取ることができるようになる。

ただし、前述のとおり場合によって(L)(R)とJoypad1・2の対応が変わってしまうので、  
状況に合わせてInputManagerを設定する必要がある。

毎回設定しなおすのが面倒なので、

・(L)がJoypad1、(R)がJoypad2の場合
・(R)がJoypad1、(L)がJoypad2の場合

のInputManagerの設定をコピーしておき、必要に応じて上書きすることにした。  
ProjectSettings/InputManager.assetを置き換えれば動くはず。  
（エディタスクリプトとかで自動化するといいかんじかも）  

あと、スティックのどれかの入力が、エディタでは正しく取れるのに  
HoloLensにつないだ場合にうまく取れなかった気がする。  
当時いろいろ調べてみたけど解決できず。。今は修正されてることに期待。

# 注意
結構前に試したので、最新の環境だと状況が違うかもしれません。  
使ったUnityのバージョンは5.5.0f3です。