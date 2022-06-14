# Mutating Maps

map m の操作を見ていきましょう。

m へ要素(elem)の挿入や更新:

```go
m[key] = elem
```

要素の取得:

```go
elem = m[key]
```

要素の削除:

```go
delete(m, key)
```

キーに対する要素が存在するかどうかは、2つの目の値で確認します:

```go
elem, ok = m[key]
```

```go
もし、 m に key があれば、変数 ok は true となり、存在しなければ、 ok は false となります<br>
なお、mapに key が存在しない場合、 elem はmapの要素の型のゼロ値となります<br>
Note: もし elem や ok をまだ宣言していなければ、次のように := で短く宣言できます<br>
```

```go
elem, ok := m[key]
```

```go
package mian //パッケージを宣言

import "fmt"　//fmtパッケージをインポート

func main() {
    m := make(map[string]int)　//make　スライスを定義　map　キーと値とを関連付け intその箱には（桁数の大きくない）整数を入れて良いよと決まり
    
    m["Answer"] = 42　　//要素の取得
	fmt.Println("The value:", m["Answer"])

	m["Answer"] = 48　//要素の取得
	fmt.Println("The value:", m["Answer"])

	delete(m, "Answer")　　//要素の削除
	fmt.Println("The value:", m["Answer"])

	v, ok := m["Answer"]　//もしmにAnswerがあれば変数okはtrueで、存在しなければfalseとなる
	fmt.Println("The value:", v, "Present?", ok)
}

出力結果
The value: 42
The value: 48
The value: 0
The value: 0 Present? false
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

<a href="https://github.com/morimotoyuuki111/Go3/blob/main/Map%20literals.md">前回　　Map literals</a>


