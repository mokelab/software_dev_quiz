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
