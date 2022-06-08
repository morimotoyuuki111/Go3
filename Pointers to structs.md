# Pointers to structs

structのフィールドは、structのポインタを通してアクセスすることもできる<br>

フィールド X を持つstructのポインタ p がある場合、フィールド X にアクセスするには (*p).X のように書くことができます。 しかし、この表記法は大変面倒ですので、Goでは代わりに p.X と書くこともできる<br>

```go
package main　//パッケージを宣言

import "fmt"　//fmtパッケージをインポート

type Vertex struct {　　//type Vertex（構造体の名前） struct
    X int　　//int型の変数　
    Y int　//int型の変数　　
}

func main() {
  v := Vertex{1,2}　//int型の変数XYがまとまった
  p := &v　　//変数pに&vが代入される。　v := Vertex{1,2}のこと
  p.X = 1e9　//p.Xに1e9が代入される　　1e9は1000000000のこと
  fmt.Println(v)　//変数pに&vが代入されているためpとvが出力される
}

出力結果
{1000000000 2}
```

- 1e9<br>
<a href="https://qiita.com/3utama/items/dd69541fedbfd6d1b7e9">参考サイト</a><br>

- 構造体<br>
プログラミング言語における変数の型のひとつで、<br>中身の構造を自分で決められる型のこと<br>
プログラミング言語における「その箱にはどんな種類の物を入れて良いか」<br>な決まりのひとつで、
中に入れられる物の種類や数を自分で決められるやつのこと<br>
<a href="https://wa3.i-3-i.info/word13243.html">参考サイト</a>

<a href="https://qiita.com/Yarimizu14/items/e93097c4f4cfd5468259">StructのField名で注意すること</a><br>

- int型<br>
<a href="https://wa3.i-3-i.info/word14966.html">参考サイト</a><br>


- パッケージ<br>
 Goには予め用意されている標準パッケージがあり、標準パッケージを利用する事で、プログラミングを効率良く行うための便利な機能<br>
 ※fmtパッケージはコンソールを出力するパッケージ※<br>
  
- インポート　<br>
取り込む、持ち込む、などの意味<br>
 
- func main<br>
 メイン関数という意味<br>
    
- 関数<br>
関数とは複数の処理をまとめておくこと<br>

- 変数の定義
```go
  func main(){ //プログラムをコンパイルして実行すると、まず main パッケージの中にある main()関数が実行される
  i := 2
  fmt.Println(i)  // 2が出力される
}
```
<a href="https://y-hiroyuki.xyz/go/variable/what-is-variable">参考サイト</a>


- 関数の定義
```go
func 関数名(){
 //処理内容
}
```
- func　関数名で関数の宣言を行う<br>
- ()内には引数を指定しますが今回の内容では、引数は使用しないので、()の中は空のままにしておく<br>
- 2行目の関数の処理内容は関数を呼び出しを行った際に実行される<br>

- main関数<br>
プログラムの最初に呼び出される関数<br>
<a href="https://zenn.dev/kubo_programmer/articles/990891ff3a43c5">参考サイト</a>

- 引数<br>
引数とは、関数に渡す値<br>
引数を使用する場合は「func 関数名(引数名 型)」と記述する事で、引数を呼び出し先の値<br>

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Struct%20Fields.md#struct-fields">前回　Struct Fields</a>
