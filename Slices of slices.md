# Slices of slices


スライスは、他のスライスを含む任意の方を含むことができる<br>

```go
pacakage main //パッケージを宣言

import (　//fmtパッケージを宣言　stringsパッケージを宣言
    "fmt"
    "strings"
)

func main() {
    // Create a tic-tac-toe board.
    board := [][]string{  //boardの中に[][]stringが代入される(string型)
      []string{"_", "_", "_"},　
      []string{"_", "_", "_"},
      []string{"_", "_", "_"},
    }
    
    // The players take turns.
    board[0][0] = "X"
    board[2][2] = "O"
    board[1][2] = "X"
    board[1][0] = "O"
    board[0][2] = "X"
    
    for i :=0; i < len(board); i++ //i :=0;　変数の初期化　 i <= len(board); i++ 変数の更新
      fmt.Printf(%s\n",strings.Join(board[i]," "))
   }
}

出力結果
X _ X
O _ X
_ _ O

```

- lenは配列の長さ<br>
