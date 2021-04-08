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

### GPIOピン  
40ピン存在する。  
General purpose input output  

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
## Linuxの世界  
2大重要事項  
- データは全て「ファイル」で保存される  
- プログラムは「プロセス」単位で動く  
その他  
- ファイルもプロセスも木構造で管理されている  
  
### apt  
APT, Advanced Packaging Tool  
---
### command (1/2)
```  
ls /bin/ | grep ls  
echo unko | rev | grep -o .  
find aaa  
grep ubuntu /etc/passwd  
find /  
find / | less  
find / | grep passwd  
'/passwd$'  
cat /etc/services | grep '[^0-9]80/'  
cat /etc/services | grep -C1 '[^0-9]80/'  
```  
---
### command (2/2)
通信系  
ping、通信先にパケットが届くか確認する  
```  
ping www.yahoo.co.jp  
ping 8.8.8.8    (google)  
ip addr show  
traceroute 8.8.8.8  
```  
マシン間でファイルをコピー！  
srp,rsync（バックアップ）  
```  
scp record_weight.sh ubuntu@192.168.3.7:~/  
rsync -av ./scraping/ ubuntu@192.168.3.7  
  
```  
---
## スライド３
### スライド３
４ページ目

* リンクを貼る

__[Google](https://www.google.co.jp/)__