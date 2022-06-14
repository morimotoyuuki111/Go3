# Function values

関数も変数です。他の変数のように関数を渡すことができます<br>

関数値( function value )は、関数の引数に取ることもできますし、戻り値としても利用できます<br>

```go
package main

import ( 
	"fmt"
	"math"
)

func compute(fn func(float64, float64) float64) float64 {
	return fn(3, 4)
}

func main() {
	hypot := func(x, y float64) float64 {
		return math.Sqrt(x*x + y*y)
	}
	fmt.Println(hypot(5, 12))

	fmt.Println(compute(hypot))
	fmt.Println(compute(math.Pow))
}
出力結果
13
5
81
```

<a href="https://cipepser.hatenablog.com/entry/2017/02/18/030554">参考記事</a><br>

