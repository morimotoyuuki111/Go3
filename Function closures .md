# Function closures

Goの関数は クロージャ( closure ) です。 クロージャは、それ自身の外部から変数を参照する関数値です。 この関数は、参照された変数へアクセスして変えることができ、その意味では、その関数は変数へ"バインド"( bind )されています。<br>

例えば、 adder 関数はクロージャを返しています。 各クロージャは、それ自身の sum 変数へバインドされます。<br>

```go
package main　//パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func adder() func(int) int { //adder関数はクロージャ関数　
    sum := 0  //sumに0が代入　
    return func(x int) int {　//return func(x int) intは入ってきた値が出てく?
         sum += x　 sumに0が代入される
         return sum //sumの値が出てく?
    }
}

func main() {
    pos, neg := adder(),adder()　//negは対極
    for i := 0; i < 10; i++ {　//i := 0;変数の初期化　i　< 10;繰り返しの条件　 i++変数の更新
        fmt.Println(
            pos(i)　//出力結果がわからない
            neg(-2*i),
        )
    }
}

出力結果
0 0
1 -2
3 -6
6 -12
10 -20
15 -30
21 -42
28 -56
36 -72
45 -90
```

- スライス型
```go
var a []string
var b []string // aとbの型は同一
```

- マップ型
```go
var a map[int]bool
// aとbの型は同一
var b map[int]bool
// キーの型が異なるため、aとcの型は異なる
var c map[int32]bool
// 要素の型が異なるため、aとdの型は異なる
var d map[int]string

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Mutating%20Maps.md#mutating-maps">前回　　Mutating Maps
</a>



     
