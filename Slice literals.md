# Slice literals

スライスのリテラルは長さのない配列リテラルのようなもの<br>
これは配列リテラル<br>

- リテラルについて<br>
<a href="https://wa3.i-3-i.info/word15346.html">参考サイト</a><br>


```go
[3]bool{true, true, false}
```

上記と同様の配列を作成し、それを参照するスライスを作成<br>

```go
[]bool{true, true, false}
```


```go

package main//パッケージ

import "fmt"　//fmtパッケージをインポート

func main(){
    q := []int{2, 3, 5, 7, 11, 13 //変数qに[]int{2, 3, 5, 7, 11, 13}が代入される
    fmt.Println(q)　//変数qが出力される
    
    r := []bool{true,false,true,true, false, true}　　//変数rに[]bool{true,false,true,true, false, true}が代入される
    fmt.Println(r) //変数rが出力される
    
    s := []struct {　//変数sに[]struct、i int　b　boolが代入される。structでiとbをまとめている
        i int
        b bool
    }{
        {2, true},
        {3, false},
        {5, true},
        {7, true},
        {11, false},
        {13, true},
     }
     fmt.Println(s)
}

出力結果
[2 3 5 7 11 13]
[true false true true false true]
[{2 true} {3 false} {5 true} {7 true} {11 false} {13 true}]
```

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Slices%20are%20like%20references%20to%20arrays.md">前回　Slices are like references to arrays</a>


