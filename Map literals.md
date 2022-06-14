# Map literals

mapリテラルは、structリテラルに似ていますが、 キー ( key )が必要です。

```go
package mian　//パッケージを宣言

import "fmt"　fmtパッケージをインポート

type Vertex struct {　　//　Vertex構造体の名前　structは構造体
    Lat,Long float64　//変数名
}

var m = map[string]Vertex{　　　//mを定義　  stringは文字列を入れていいよと意味なので"Bell Labs"
    "Bell Labs": Vertex{　　　// Vertexには40.68433, -74.39967
        40.68433, -74.39967,
	},
  "Google": Vertex{ //stringは文字列を入れていいよと意味なので "Google"
		37.42202, -122.08408,　//37.42202, -122.08408
	},
}

func mian() {
  fmt.Println(m)　
}　

出力結果
map[Bell Labs:{40.68433 -74.39967} Google:{37.42202 -122.08408}]
```

- 構造体<br>
<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Structs.md">過去の勉強</a><br>

- 配列<br>
<a href="https://web-camp.io/magazine/archives/62260">参考サイト</a><br>
<a href="https://wa3.i-3-i.info/word11924.html">参考サイト</a><br>

- bool型<br>
<a href="https://golang.keicode.com/basics/go-data-types.php#3">参考サイト</a><br>

- 素数<br>
<a href="https://ja.wikipedia.org/wiki/%E7%B4%A0%E6%95%B0">参考サイト</a><br>

- int型<br>
<a href="https://wa3.i-3-i.info/word14966.html">参考サイト</a><br>

- string型<br>
<a href="https://wa3.i-3-i.info/word14965.html">参考サイト</a><br>

- パッケージ<br>
 Goには予め用意されている標準パッケージがあり、標準パッケージを利用する事で、プログラミングを効率良く行うための便利な機能<br>
 ※fmtパッケージはコンソールを出力するパッケージ※<br>
  
- インポート　<br>
取り込む、持ち込む、などの意味<br>

- func main<br>
 メイン関数という意味<br>
    
- 関数<br>
関数とは複数の処理をまとめておくこと<br>

- 変数の定義<br>
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Maps.md">前回　 Maps</a>


