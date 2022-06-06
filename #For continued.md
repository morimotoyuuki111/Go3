初期化と後処理ステートメントの記述は任意<br>

```go
package main　//パッケージを宣言
import "fmt"標準パッケージをインポート　(fmtパッケージをインポートしている)

func main() {
	sum := 1　　//初期値が１
	for ; sum < 1000; {　  //繰り返しの条件　　sumの中が1000より小さい間、繰り返す　　		
  sum += sum //sumの中にsumを足して代入する
  
	}
	fmt.Println(sum)　変数sumを出力
}

出力結果
1024
```
For is Go's "while"
※for ; sum部分のセミコロンを省略して書くこともできる<br>
For文
<a href="https://wa3.i-3-i.info/word15412.html">参考サイト</a>
<a href="https://java2005.cis.k.hosei.ac.jp/materials/lecture04/for.html">参考サイト</a>

- +=演算子（加算）（変数と式の和を変数に代入する）

- package main<br>
 パッケージを宣言のこと<br>
 
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/For.md">前回For</a>


