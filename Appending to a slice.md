# Appending to a slice


スライスへ新しい要素を追加するには、Goの組み込みの append を使います<br>


```go
func append(s []T, vs ...T) []T

```

append への最初のパラメータ s は、追加元となる T 型のスライス。残りの vs は、追加する T 型の変数群<br>

append の戻り値は、追加元のスライスと追加する変数群を合わせたスライス<br>

元の配列 s が、変数群を追加する際に容量が小さい場合は、<br>
より大きいサイズの配列を割り当て直す<br>
その場合、戻り値となるスライスは、新しい割当先を示す<br>

```go
package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main() {
	var s []int //[]intはintが入ったスライス　varは定義　
	printSlice(s)　　//printSliceは自分が作った関数。

	// append works on nil slices.
	s = append(s, 0) //変数sにappend(s, 0)が代入される
	printSlice(s)　

	// The slice grows as needed.
	s = append(s, 1)　//変数sにappend(s, 1)が代入される
	printSlice(s)

	// We can add more than one element at a time.
	s = append(s, 2, 3, 4)　　　//sには0,1が入っている
	printSlice(s)
}

func printSlice(s []int) {　
	fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)　//len(s)は要素の数　、cap(s), sはその配列に格納できる要素の数
}

出力結果
len=0 cap=0 []　//空
len=1 cap=1 [0]
len=2 cap=2 [0 1]
len=5 cap=6 [0 1 2 3 4]

```

- Creating a slice with makeについて<br>
<a href="https://zenn.dev/tomi/articles/2020-09-29-go-4">参考サイト</a><br>


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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Slices%20of%20slices.md">前回　Slices of slices</a>

