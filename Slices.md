# Slices

配列は固定長です。一方で、スライスは可変長です。より柔軟な配列と見なすこともできる.実際には、スライスは配列よりもより一般的<br>

型 []T は 型 T のスライスを表す<br>

コロンで区切られた二つのインデックス low と high の境界を指定することによってスライスが形成される:

```go
a[low : high]
```

これは最初の要素は含むが、最後の要素は除いた半開区間を選択する<br>

次の式は a の要素の内 1 から 3 を含むスライスを作る<br>

```go
a[1:4]
```

```go
package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main() { 
  primes :=[6]int{2, 3, 5, 7, 11, 13} //変数primesの中に[6]int{2, 3, 5, 7, 11, 13}が代入
  
  var s []int = primes[1:4]　// varは定義　　変数sの中にprimes[1:4]が代入
  fmt.Println(s) 
}
[3 5 7]
```

スライスについて
<a href="https://golang.keicode.com/basics/go-slice.php#1">参考サイト</a><br>


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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Arrays.md">前回　Arrays</a>


