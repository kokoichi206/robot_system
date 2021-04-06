# ロボットシステム学講義
- 上田隆一さんの[youtube](https://www.youtube.com/watch?v=twM88vv21LM&list=PLbUh9y6MXvjdIB5A9uhrZVrhAaXc61Pzz&index=1)のノート

## 開発における手っ取り早さの実現
プラットフォームの存在
- ハード：PC、Raspberry Pi、Arduino
- ソフト：UNIX、Linux
- サービス：GitHub
- ロボット：TurtleBot、Cart-mini、HSR、

## Raspberry Pi
シングルボードコンピュータ
性能というよりもプラットフォームとして非常に優秀
イギリスで開発された教育用のシングルボードコンピュータ
安価でハードの制御ができるような目的、2009-
2016に1000万台販売

## 講義の目的
1つのシングルボードコンピュータを深く理解
- 低レイヤー
    - OSの仕組み
    - デバイスドライバ作成
- 高レイヤー
    - ROSのモジュール作成
- 社会的レイヤー
    - 開発方法（Git、GitHub）
    - 著作権やライセンス
    
### 必要なもの
- USBケーブル
- microSDカード（16GB）
- LANケーブル

## Install Ubuntu on Raspberry Pi
ubuntu Raspberry pi と Etcherを利用

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

## GPIOピン
40ピン存在する。
General purpose input output

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

## Linuxの世界
2大重要事項
- データは全て「ファイル」で保存される
- プログラムは「プロセス」単位で動く
その他
- ファイルもプロセスも木構造で管理されている

### command
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

### apt
APT, Advanced Packaging Tool



## Git
バージョン管理システム
Linus Torvalds が作成
- Linusさんぶちぎれがち。
- 有料化にキレて2週間でGit作った。

初期設定
```
git config --global user.name "mi"
git config --global user.email "tt.300607@gmail.com"
git config --global core.editor vim
cat .gitconfig
```

## GitHub
Gitを利用したサービス
「リポジトリ」のホスティングと公開、コミュニケーション
```
git clone https://github.com/kokoichi206/robot_system.git
``` 


## やりたいこと
- /etc/vim をいじる
- vimtutor



