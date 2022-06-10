# Slices are like references to arrays

スライスは配列への参照のようなもの<br>
スライスはどんなデータも格納しておらず、単に元の配列の部分列を指し示している<br>
スライスの要素を変更すると、その元となる配列の対応する要素が変更される<br>
同じ元となる配列を共有している他のスライスは、それらの変更が反映される<br>

```go
package main //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main() {　
    names := [4]string{ //変数namesに配列[4] "John","Paul","George","Ringo",が代入される　string型
        "John",
        "Paul",
        "George",
        "Ringo",
    }
    fmt.Println(names) //変数namesが出力される
    
    a := names[0:2] //変数aにnames[0:2]が代入される。元の入れる部分になるため[John Paul]
    b := names[1:3]//変数bにnames[1:3]が代入される。a同様に元の入れる部分のため[Paul George]
    fmt.Println(a,b) //変数a,bが出力される
    
    b[0] = "XXX" //変数b[0]に"XXX"がされる
    fmt.Println(a, b)//bにXXXが代入されているため　aがjohn bがXXX
    fmt.Println(names) //変数namesが出力される
}

出力結果
[John Paul George Ringo]
[John Paul] [Paul George]
[John XXX] [XXX George]
[John XXX George Ringo]
```
スライスについて<br>
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Slices.md">前回　Slices</a>




