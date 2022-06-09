# Arrays
[n]T 型は、型 T の n 個の変数の配列( array )を表す<br>

以下は、intの10個の配列を宣言している<br>

```go
var a [10]int
```

配列の長さは、型の一部分です。ですので、配列のサイズを変えることはできません。 これは制約のように思えますが、心配しなくてOk<br>Goは配列を扱うための便利な方法を提供している<br>

```go

package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main(){　
  var a [2]string　//　a[0] a[1]が入ってる？　　varは定義　stringは文字列を入れ良いよと決まりがある
  a[0] = "Hello"　　//a[0]にHelloが代入される
  a[1] = "World"　　//a[1]にWoldが代入される
  fmt.Println(a[0], a[1])　// Hello　　Worldが出力される
  fmt.Println(a) aに　配列[0]にHello [1]にWorldが代入されているので[Hello World]が出力される
  
  
  primes := [6]int{2, 3, 5, 7, 11, 13}　　//変数primesの中に[6]が代入されている。６つの配列の中に{2, 3, 5, 7, 11, 13}　が入っている
    fmt.Println(primes)　　/primesが出力されているため[2 3 5 7 11 13]が出力される
  }
  
出力結果
Hello World
[Hello World]
[2 3 5 7 11 13]
```

- 素数<br>
<a href="https://ja.wikipedia.org/wiki/%E7%B4%A0%E6%95%B0">参考サイト</a><br>

- int型<br>
<a href="https://wa3.i-3-i.info/word14966.html">参考サイト</a><br>

- string<br>
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Struct%20Literals.md">前回　Struct Literals</a>



  
