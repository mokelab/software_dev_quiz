# Goの基礎的なやつ

## 1 Hello world

1-1 以下は `main.go` ファイルである。 `go run main.go` で実行すると `Hello Go World!` と表示されるGoプログラムとなるよう、空欄には何をいれる？

```go
package main

import "fmt"

[ 空欄 ] {
	fmt.Println("Hello Go World!")
}
```

1-2 Goで書かれたプログラムをビルドし、実行可能ファイルを作るには、どんなコマンドを実行する？

## 2 変数や定数


2-1 `int` 型の変数 `a` を作り、それに1848を代入して表示するGoプログラムにしたい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	[ 空欄 ]
	a = 1848
	fmt.Printf("a=%d\n", a)
}
```

2-2 2-1 のプログラムは1行減らすことができる。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	a [空欄] 1848
	fmt.Printf("a=%d\n", a)
}
```

2-3 定数 `url` を作りたい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	[ 空欄 ] url = "https://mokelab.com/ja"
	fmt.Printf("url=%s\n", url)
}
```

## 3 基本型

基本型ぐらいは調べずさっと型名が言えたほうがいいと思う。。。

3-1 ビルドターゲットは32bitシステムである。64ビット符号付き整数な変数 `num` を定義したい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	var num [ 空欄 ] = 123456789012
	fmt.Printf("num=%d\n", num)
}

```

3-2 倍精度浮動小数点型の変数 `pi` を作りたい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	// https://pkg.go.dev/math
	var pi [ 空欄 ] = 3.14159265358979323846264338327950288419716939937510582097494459
	fmt.Printf("pi=%f\n", pi)
}
```

3-3 空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	var b [ 空欄 ] = false
	fmt.Printf("b=%t\n", b)
}
```
