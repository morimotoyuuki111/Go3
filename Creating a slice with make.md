# Creating a slice with make

スライスは、組み込みの make 関数を使用して作成することができます。 これは、動的サイズの配列を作成する方法です。<br>

make 関数はゼロ化された配列を割り当て、その配列を指すスライスを返します。<br>

```go
a := make([]int, 5)  // len(a)=5
```
make の3番目の引数に、スライスの容量( capacity )を指定できます。 cap(b) で、スライスの容量を返します:<br>

```go
b := make([]int, 0, 5) // len(b)=0, cap(b)=5

b = b[:cap(b)] // len(b)=5, cap(b)=5
b = b[1:]      // len(b)=4, cap(b)=4
```

```go
package main //パッケージを宣言

import "fmt"

func main() {
	a := make([]int, 5)　//変数a に　make([]int, 5)が代入
	printSlice("a", a)

	b := make([]int, 0, 5) //bにmake([]int, 0, 5)が代入
	printSlice("b", b)　

	c := b[:2] //cにb[:2]が代入される
	printSlice("c", c)

	d := c[2:5] //dにc[2:5]が代入される
	printSlice("d", d)
}

func printSlice(s string, x []int) { //xは要素数?　%sは文字列、string型変数や定数を宣言し初期化、[]intはこの箱には（桁数の大きくない）整数を入れて良いですよと意味
	fmt.Printf("%s len=%d cap=%d %v\n", 
           s, len(x), cap(x), x)
}

出力結果
a len=5 cap=5 [0 0 0 0 0] //配列の中に入っている要素の数がlen　//配列に格納出来る要素の数がcap
b len=0 cap=5 []
c len=2 cap=5 [0 0]
d len=3 cap=3 [0 0 0]
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Nil%20slices.md">前回　Nil slices</a>
