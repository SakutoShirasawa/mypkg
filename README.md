# mypkg  
[![test](https://github.com/SakutoShirasawa/ros2/actions/workflows/test.yml/badge.svg)](https://github.com/SakutoShirasawa/ros2/actions/workflows/test.yml)  

このリポジトリは、talkerが起動してからのカウントをlistenerで確認することができます。  

## 実行方法  
＊必ずros2がインストールされている環境で行ってください。  
1.自分のワークスペースからros2_wsに移動する  
```
cd ros2_ws
```
2.ros2_wsからsrcというディレクトリに移動する  
```
cd src
```
3.以下のコマンドを使用し、このリポジトリを手元の環境にクローンする  
```
git clone git@github.com:SakutoShirasawa/mypkg.git
```
4.手元の環境に正常にクローンされたかを確認する
```
ls
```
5.以下のコマンドを使用してワークスペースに移動し、ビルドする  
```
cd ~/ros2_ws  
colcon build  
source ~/.bashrc  
```
6.もう一つ端末を用意し、実行する  
＊端末１  
```
cd ~/ros2_ws  
ros2 run mypkg talker  
```

＊端末２  
```
cd ~/ros2_ws
ros2 run mypkg listener
```
## 実行結果  
[INFO] [Listener]: Listen: 34  
[INFO] [Listener]: Listen: 35  
[INFO] [Listener]: Listen: 36  
[INFO] [Listener]: Listen: 37  
[INFO] [Listener]: Listen: 38  
[INFO] [Listener]: Listen: 39  
・・・  
端末１に何も表示がないのは正常に動作しているということです  

## 必要なソフトウェア  
python テスト済み：3.7～3.10  

## テスト環境  
・Ubuntu22.04.3LTS  

## 権利  
 ＊ このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
 ＊ © 2023 SakutoShirasawa












## コマンドの詳細内容  
*talker ・・・起動するとカウントを始め、出力するノード  

*listener・・・publisherから出力されたカウントを標準出力するノード  

*トピック・・・talkerが起動してから計測したカウントの数値  

