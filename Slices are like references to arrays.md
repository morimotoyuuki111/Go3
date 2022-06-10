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



