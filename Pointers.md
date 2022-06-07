#

Goはポインタを扱います。 ポインタは値のメモリアドレスを指す<br>

変数 T のポインタは、 *T 型で、ゼロ値は nil<br>

```go
var p *int
& オペレータは、そのオペランド( operand )へのポインタを引き出します。

i := 42
p = &i
* オペレータは、ポインタの指す先の変数を示します。

fmt.Println(*p) // ポインタpを通してiから値を読みだす
*p = 21         // ポインタpを通してiへ値を代入する
これは "dereferencing" または "indirecting" としてよく知られています。

なお、C言語とは異なり、ポインタ演算はない。
```

```go

package main //パッケージを宣言

import "fmt"　//fmtパッケージを宣言

func main(){
  i, j := 42,2701　 //変数　i に４２、変数　j に27０１が代入される
  
  p := &i　// 変数pに　＆iが代入される
  fmt.Println(*p)
the pointer　//ポインタ変数
    *p = 21　　/*pに　２１が代入されるその後にiへ渡す
the pointer　//ポインタ変数
    fmt.Println(i)
value of i　//iの値

    p = &j
    *p = *p / 37
the pointer
    fmt.Println(j)
of j
}

出力結果
42
21
73

```
