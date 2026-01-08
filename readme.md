C107 配布基板サポート
今宵＠たまはい　で頒布した基板の説明です。

## マイコンをさす想定
![alt text](mcu_ptn.PNG) 
![alt text](mcu_ptn2.PNG) 
![alt text](mcu_ptn3.PNG) 

# GND, 3.3V
![alt text](gnd-1.PNG) 
![alt text](v33.PNG) 

# スイッチ、可変抵抗
可変抵抗
![alt text](mcu_vr.PNG) 
スイッチ


# ユニバーサルパターン
![alt text](univ.PNG) 
LCDやoled接続にも。

# LEDドライバ(HT33K16を使う場合)
マイコンが3.3V動作であることを想定し、PCA9306のI2Cレベルシフタを使います。
![alt text](leddriver.PNG) 

PCA9306にはパッケージ違いがあるので、好きなのを使ってください。
!!! 同じパッケージでピン配置違いがあります。対応してないのは…ごめんなさい
![alt text](pca9306-f.PNG) 
![alt text](pca9306-b.PNG) 

## 基板修正が必要です!
Vref2を間違えました。使った9306に応じて。　
![alt text](pca9306_mod_f.PNG) 
![alt text](pca9306_mod.PNG)

