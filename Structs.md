Structs.md


struct (構造体)は、フィールド( field )の集まり<br>

```go
package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

type Vertex struct {　 //type Vertex（構造体の名前） struct
  X int　 //int型の変数　Xに１
  Y int　　//int型の変数　　Yに２
}

func main() {
  fmt.Println(Vertex{1,2})　　//{1,2}が出力される
  }
```

- 構造体<br>
プログラミング言語における変数の型のひとつで、<br>中身の構造を自分で決められる型のこと<br>
プログラミング言語における「その箱にはどんな種類の物を入れて良いか」<br>な決まりのひとつで、
中に入れられる物の種類や数を自分で決められるやつのこと<br>
<a href="https://wa3.i-3-i.info/word13243.html">参考サイト</a>

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Stacking%20defers.md">前回　Stacking defers</a>
