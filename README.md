# ロボットシステム学講義  
- 上田隆一さんの[youtube](https://www.youtube.com/watch?v=twM88vv21LM&list=PLbUh9y6MXvjdIB5A9uhrZVrhAaXc61Pzz&index=1)のノート  
  
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
  

## markdown to slide  
- gitHub pages の利用  
    - [見た目のイメージ](https://kokoichi206.github.io/robot_system/first)  

[このサイト](https://qiita.com/natsumo/items/717e40de2c43824624b6)を参考にしたら、markdownでスライドを表示できるようにはなった。  

## markdownのファイルの改行の前に半角スペース2ついれるshellScript  
- 目的：vscodeのプレビューだと改行前にスペース入れなくても正しく改行されるが、giHub pagesにアップしたときは（普通は）そうではない  

[参考](https://qiita.com/hirohiro77/items/7fe2f68781c41777e507)（sedでスペース置換を探してたら見つけた）  
> #よく間違うのが's/\n/\r\n/'では置換出来ないので注意  
sed -i -e 's/$/\r/' source.txt  

実際のコード  
```markdownSpace.sh  
#/bin/bash

# echo $1
fileName=`echo $1 | sed 's/\.[^\.]*$//'`
# echo $fileName
# cat $1 | tr '\n' '  \n' > ${fileName}_revised.md
sed 's/$/  /g' $1 > ${fileName}_rev.md
```  

- $（行末）を\r（CR）で変換しているのに、その結果が\r\n（CR＋LF）になっている点が不思議だが、これはパターンスペースのしわざである  
- 「sedは読み込んだ行の行末にある改行を削除してパターンスペースと呼ばれるバッファに格納したうえでテキスト処理をし、最後にパターンスペースの内容に改行をつけて出力する」  


