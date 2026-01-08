C107 配布基板サポート
今宵＠たまはい　で頒布した基板の説明です。

使ってみた

![alt text](<スクリーンショット 2026-01-08 230304-1.png>) 

## マイコンをさす想定
![alt text](mcu_ptn.PNG) 
![alt text](mcu_ptn2.PNG) 
![alt text](mcu_ptn3.PNG) 

Arduinoならこんな感じ

![alt text](<スクリーンショット 2026-01-09 001336-1.png>)

# GND, 3.3V
![alt text](gnd-1.PNG) 
![alt text](v33.PNG) 

# スイッチ、可変抵抗
可変抵抗
![alt text](mcu_vr.PNG) 

スイッチ

内部プルアップされたGPIOにつなぐ想定

スイッチのパターンの片方はGNDに接続済みです。

使うスイッチがどう結線されてるか確認してね

記事最初の写真のように、千鳥に配置できるパターンです。
![alt text](sw-1.PNG)



# ユニバーサルパターン
![alt text](univ.PNG) 
LCDやoled接続にも。

# LEDドライバ(HT33K16を使う場合)
マイコンが3.3V動作であることを想定し、PCA9306のI2Cレベルシフタを使います。

この場合、3.3V（マイコン）側のI2Cのプルアップは無し、  
5V側のSDA,SCLを1kΩで5Vにプルアップしてください。

![alt text](<スクリーンショット 2026-01-09 003057-1.png>)

こんな感じ

![alt text](leddriver.PNG) 

PCA9306にはパッケージ違いがあるので、好きなのを使ってください。
!!! 同じパッケージでピン配置違いがあります。対応してないのは…ごめんなさい
（表面に実装できるパッケージ）
![alt text](pca9306-f.PNG) 
（ *裏* 面に実装できるパッケージ）
![alt text](pca9306-b.PNG) 

## 基板修正が必要です!

Vref2を間違えました。使った9306に応じて。　
- 表
![alt text](pca9306_mod_f.PNG) 
- 裏
![alt text](pca9306_mod.PNG)

