# Nil slices

スライスのゼロ値は nil <br>
nil スライスは 0 の長さと容量を持っており、何の元となる配列も持っていない<br>

```go
package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main() {
  var s[]int　//varは定義  s[]を定義
  fmt.Println(s, len(s), cap(s))　 //s[]を出力。[]は空なので[]と出力される。len(s),cap(s)を出力。sは何も代入されていないため0
  
  if s == nil //もしもsの中が0だったらnil!と出力してねと意味
      fmt.Println("nil!")
  }
}
```

- Printfについて<br>
<a href="https://golang.keicode.com/basics/go-print-basics.php#2">参考サイト</a><br>

- スライスの長さと容量について<br>
<a href="https://y-hiroyuki.xyz/go/slice/len-cap">参考サイト</a><br>

- 配列<br>
<a href="https://web-camp.io/magazine/archives/62260">参考サイト</a><br>
<a href="https://wa3.i-3-i.info/word11924.html">参考サイト</a><br>


- bool型<br>
<a href="https://golang.keicode.com/basics/go-data-types.php#3">参考サイト</a><br>

- スライスについて<br>
<a href="https://golang.keicode.com/basics/go-slice.php#1">参考サイト</a><br>

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Slice%20length%20and%20capacity.md">前回　Slice length and capacity</a>
