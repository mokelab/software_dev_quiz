# Goの基礎的なやつ

※空欄には「何も記述しない」ケースもあります。

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

3-4 `10 / 3` の整数部分だけを取り出したい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	f := 10 / 3
	var a int = [ 空欄 ] // fの整数部分だけ取り出したい
	fmt.Printf("a=%d\n", a)
}
```

## 4 条件分岐

4-1 変数 `cp` の値が1500以下の時は `出場可能` を表示し、そうでない場合は `出場不可` を表示するGoプログラムにしたい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	// 出典：ポケモンGO「スーパーリーグ」
	cp := 1499
	[ 空欄 ] {
		fmt.Println("出場可能")
	} else {
		fmt.Println("出場不可")
	}
}
```

4-2 変数 `w` の値が23以下の時は `1週目` を表示し、 24以上46以下の時は `2週目` を表示し、それ以外は `3週目` を表示するGoプログラムにしたい。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	// 出典：リングフィットアドベンチャー「アドベンチャーモード」
	w := 41
	if w <= 23 {
		fmt.Println("1週目")
	} [ 空欄 ] {
		fmt.Println("2週目")
	} else {
		fmt.Println("3週目")
	}
}
```

4-3 変数 `hand` はジャンケンの手を表す変数である。空欄1と空欄2には何をいれる？

```go
package main

import "fmt"

func main() {
	hand := 1
	[ 空欄1 ] {
	case 0:
		fmt.Println("グー")
		[ 空欄2]
	case 1:
		fmt.Println("チョキ")
		[ 空欄2]
	case 2:
		fmt.Println("パー")
		[ 空欄2]
	default:
		fmt.Println("その手はなに？")
		[ 空欄2]
	}
}
```

4-4 モケラさんは指定した月が何日あるかを表示するGoプログラムを書いた。ビルドはできたようである。問題点がなければ「問題なし」と解答し、問題点があるようであればその点を指摘してください。

```go
package main

import "fmt"

func main() {
	month := 1 // 1-12とする
	var day int
	switch month {
	case 1: // 1月
	case 3: // 3月
	case 5:
	case 7:
	case 8:
	case 10:
	case 12:
		day = 31
	case 2:
		day = 29 // 29日が選択肢にあれば大丈夫やろ。。。
	case 4:
	case 6:
	case 9:
	case 11:
		day = 30
	}
	fmt.Printf("%d 月は %d 日まであるよ", month, day)
}
```

4-5 4-2を書き換えてみた。空欄には何をいれる？

```go
package main

import "fmt"

func main() {
	// 出典：リングフィットアドベンチャー「アドベンチャーモード」
	w := 41
	[ 空欄 ] {
	case w <= 23:
		fmt.Println("1週目")
	case w <= 46:
		fmt.Println("2週目")
	default:
		fmt.Println("3週目")
	}
}
```

## 5 繰り返し

5-1 1から10まで順に表示するGoプログラムにしたい。空欄に入れるものは？

```go
package main

import "fmt"

func main() {
	[ 空欄1 ] i := 1; [ 空欄2 ] ; i++ {
		fmt.Println(i)
	}
}
```

5-2 合計(sum)が `1000` を超えるまで繰り返すGoプログラムにしたい。空欄にいれるものは？

```go
package main

import "fmt"

func main() {
	a := 1
	b := 1
	sum := 0
	[ 空欄 ] sum < 1000 {
		sum += b
		c := a + b
		a = b
		b = c
	}
	fmt.Printf("a=%d b=%d sum=%d\n", a, b, sum)
}
```

5-3 5-2 を書き換え、繰り返し終了の条件をループ中に移動させてみた。空欄にいれるものは？

```go
package main

import "fmt"

func main() {
	a := 1
	b := 1
	sum := 0
	[ 空欄 ] {
		if sum >= 1000 {
			break
		}
		sum += b
		c := a + b
		a = b
		b = c
	}
	fmt.Printf("a=%d b=%d sum=%d\n", a, b, sum)
}
```

## 6 関数を定義する

6-1 整数をひとつ受け取り、1加えた整数値を結果として返す関数 `add1` を作りたい。空欄にいれるものは？

```go
package main

import "fmt"

func add1(v int) [ 空欄1 ] {
	[ 空欄2 ] v + 1
}

func main() {
	nextValue := add1(1005)
	fmt.Println(nextValue)
}
```

6-2 6-1を無名関数を作る例に書き換えてみた。空欄にいれるものは？

```go
package main

import "fmt"

func main() {
	add1 := [ 空欄 ] {
		return v + 1
	}
	nextValue := add1(1005)
	fmt.Println(nextValue)
}
```

6-3 負の数が渡されたらエラーを返す関数にアップグレードした。空欄には何をいれる？

```go
package main

import (
	"errors"
	"fmt"
)

func add1(v int) [ 空欄 ] {
	if v < 0 {
		return 0, errors.New("v must not be negative")
	}
	return v + 1, nil
}

func main() {
	nextValue, err := add1(1005)
	if err != nil {
		fmt.Printf("Failed to add: %s\n", err)
		return
	}
	fmt.Println(nextValue)
}
```
