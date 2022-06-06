```go
pakckage main　//パッケージを宣言
import "fmt"　fmtパッケージをインポート
func main(){
  score := 50　　//変数scoreに５０が代入される
  if score > 80{ //条件式　　//scoreが80より大きいときに成り立つ
    fmt.Println("よくできました")
  }else{　
     fmt.Println("頑張りましょう")
  }
}
出力結果　
頑張りましょう
```
 
 「もし○○ならば●●を行う、そうでなければ▲▲を行う」という条件分岐ができる<br>
 成り立つときは「true」、成り立たないときは「false」<br>
 
- elseについて<br>
<a href="https://y-hiroyuki.xyz/go/conditional-branch/else-if">参考サイト</a><br>
<a href="https://golang.keicode.com/basics/go-statement-if.php">参考サイト</a><br>

 
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
```
  func main(){ //プログラムをコンパイルして実行すると、まず main パッケージの中にある main()関数が実行される
  i := 2
  fmt.Println(i)  // 2が出力される
}
```
<a href="https://y-hiroyuki.xyz/go/variable/what-is-variable">参考サイト</a>


- 関数の定義
```
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
