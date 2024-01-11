# mypkg  
[![test](https://github.com/SakutoShirasawa/ros2/actions/workflows/test.yml/badge.svg)](https://github.com/SakutoShirasawa/ros2/actions/workflows/test.yml)  

## mypkgについて  
このリポジトリは、千葉工業大学の2023年度ロボットシステム学の講義内課題です。また、このリポジトリはros2のパッケージです。コマンドを使用する場合は、各自のワークスペースで実行してください。  
## 実行方法  
方法１　端末を２つ用意する  
- 端末１　talker
  - 以下のコマンドを使用   
```  
ros2 run mypkg talker  
```  
- 端末２　listener  
  - 以下のコマンドを使用  
```  
ros2 run mypkg listener  
```  

方法２　端末を１つ用意する  
  - 以下のコマンドを使用  
```
ros2 launch mypkg talk_listen.launch.py  
```
## 実行結果  
方法１  
```
[INFO] [1704429933.069873300] [listener]: Listen: 23
[INFO] [1704429933.561134400] [listener]: Listen: 24
[INFO] [1704429934.061915600] [listener]: Listen: 25
[INFO] [1704429934.560646200] [listener]: Listen: 26
[INFO] [1704429935.062060100] [listener]: Listen: 27
[INFO] [1704429935.560483500] [listener]: Listen: 28
[INFO] [1704429936.061981200] [listener]: Listen: 29
[INFO] [1704429936.561264000] [listener]: Listen: 30  
```  
端末１に何も表示がないのは正常に動作しているということです  

方法２  
```
[INFO] [launch]: All log files can be found below /home/sakutoshirasawa/.ros/log/2024-01-05-13-38-33-154757-DESKTOP-DOF0AUT-232
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [233]
[INFO] [listener-2]: process started with pid [235]
[listener-2] [INFO] [1704429514.042199300] [listener]: Listen: 0
[listener-2] [INFO] [1704429514.529052800] [listener]: Listen: 1
[listener-2] [INFO] [1704429515.028271600] [listener]: Listen: 2
[listener-2] [INFO] [1704429515.528794700] [listener]: Listen: 3
[listener-2] [INFO] [1704429516.028580700] [listener]: Listen: 4
[listener-2] [INFO] [1704429516.529523800] [listener]: Listen: 5
[listener-2] [INFO] [1704429517.029317000] [listener]: Listen: 6
[listener-2] [INFO] [1704429517.528651500] [listener]: Listen: 7  
```  
いずれも、Ctrl+Cで終了できます  

## ノードの詳細内容
- talker ・・・起動するとカウントを始め、出力するノード

- listener・・・talkerからcountupというトピックを通して標準出力するノード  
## トピックの説明  
- int16型のメッセージをtalkerから受け取り、listenerに渡す  

## 必要なソフトウェア  
- ros2  

## テスト環境  
- Ubuntu22.04.3LTS  

## 権利  
- このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．  
- © 2023 SakutoShirasawa
