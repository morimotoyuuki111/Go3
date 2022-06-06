defer ステートメントは、deferへ渡した関数の実行を、<br>
呼び出し元の関数の終わり(returnする)まで遅延させるもの<br>

defer へ渡した関数の引数は、すぐに評価されますが、<br>
その関数自体は呼び出し元の関数がreturnするまで実行されない<br>

```go

package main　//パッケージを宣言

import "fmt"　fmtパッケージをインポート

func main() {

  defer fmt.Println("world")　//defer　遅延 worldと出力されるが遅延されて出力される
  
  fmt.Println("hello")　//helloと出力される
}
```

- defer<br>
<a href="https://qiita.com/Ishidall/items/8dd663de5755a15e84f2">参考サイト</a><br>


- switch<br>
条件の値がcaseの値と一致するとき、処理が実行される.
caseの後ろのコロン（:）などは忘れがちなので注意<br>
<a href="https://y-hiroyuki.xyz/go/conditional-branch/switch">参考サイト</a><br>
<a href="https://golang.keicode.com/basics/go-statement-switch.php">timeパッケージチートシート</a><br>

- runtimeパッケージ<br>
<a href="https://wa3.i-3-i.info/word13467.html">参考サイト</a><br>

- timeパッケージ<br>
 <a href="https://leben.mobi/go/time/go-programming/">参考サイト</a><br>
 <a href="https://qiita.com/wMETAw/items/2c3120d1338c646ecfba">参考サイト</a><br>

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/%23Switch%20with%20no%20condition.md">前回　Switch with no condition</a>
