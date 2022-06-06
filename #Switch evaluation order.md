switch caseは、上から下へcaseを評価します。 caseの条件が一致すれば、そこで停止(自動的にbreak)。

```go
(例えば、

switch i {
case 0:
case f():
}
では、 i==0 であれば、 case 0 でbreakされるため f は呼び出されません)

Note: Go playground上の時間は、いつも "2009-11-10 23:00:00 UTC" 。
```

```go

package main //パッケージを宣言

import ( //fmtパッケージにインポート 
  "fmt" 
  "time" //ランタイムパッケージにインポート
)

func main(){
  fmt.Println（"When's Saturday?") //土曜日はいつ？
  today := time.Now().Weekday()　　//今日　今、何時　　平日
  switch time.Saturday {　　//条件式　　土曜日は何時 
  case today + 0:
    fmt.Println("Today.")
  case today + 1:
    fmt.Println("Tomorrow.")
  case today + 2:
    fmt.Println("In two days.")
  default:
    fmt.Println("Too far away.")
  }
}

出力結果
When's Saturday?　　
Too far away.

```

上記のコードは土曜日はいつと出力される<br>
条件式は土曜日は何時とあるのでcaseに当てはまるもがないため<br>
出力されるためdefaultのToo far awayが出力される<br>

- switch<br>
条件の値がcaseの値と一致するとき、処理が実行される
caseの後ろのコロン（:）などは忘れがちなので注意<br>
<a href="https://y-hiroyuki.xyz/go/conditional-branch/switch">参考サイト</a><br>
<a href="https://golang.keicode.com/basics/go-statement-switch.php">参考サイト</a><br>

- runtimeパッケージ<br>
<a href="https://wa3.i-3-i.info/word13467.html">参考サイト</a><br>

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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Switch.md">前回　Switch</a>
