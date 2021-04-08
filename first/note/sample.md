name: inverse
layout: true
class: center, middle, inverse
---
# スライド作りの練習
わくわく わくわく
---
layout:false
## 開発における手っ取り早さの実現  
プラットフォームの存在  
- ハード：PC、Raspberry Pi、Arduino  
- ソフト：UNIX、Linux  
- サービス：GitHub  
- ロボット：TurtleBot、Cart-mini、HSR、  

---
## Raspberry Pi  
シングルボードコンピュータ  
性能というよりもプラットフォームとして非常に優秀  
イギリスで開発された教育用のシングルボードコンピュータ  
安価でハードの制御ができるような目的、2009-  
2016に1000万台販売  

### Install Ubuntu on Raspberry Pi  
ubuntu Raspberry pi と Etcherを利用 

---
## ipアドレス  
```  
ip a  
```  
192.168.3.7 がラズパイのIPアドレス  
他のPCからアクセスする方法  
```  
ssh ubuntu@192.168.3.7  
=> pw: hogehoge  
```  
画面真っ暗になっても、メモリ->SSD間で書き込みをしてるため、すぐは切らない！！  
通信できてるかチェック  
```  
ping 192.168.3.7  
```  
---
## PC spec  
```  
cat /proc/cpuinfo | less  
-> j,k  
free  
ls /dev/mmcblk0*  
uname  
cat /etc/lsb-release  
ps  
ps aux (全プロセス)（[]は実はプロセスじゃない）  
top  
pstree  
pstree -a  
```  
---
## スライド３
### スライド３
４ページ目

* リンクを貼る

__[Google](https://www.google.co.jp/)__