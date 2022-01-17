# Goの構造体

## 1 基本

### 1-1

色を表す `Color` という構造体を作りたい。空欄にいれるものは？

```go
package main

import "fmt"

[ 空欄 ] {
	Red   uint8
	Green uint8
	Blue  uint8
}

func main() {
	mokeColor := Color{
		Red:   0x00,
		Green: 0xa3,
		Blue:  0x9e,
	}
	fmt.Printf("赤は%d\n", mokeColor.Red)
}
```

## 2 メソッド

### 2-1

色を表す `Color` という構造体に、16進数8桁の数値に変換する `Hex()` というメソッドを追加したい。空欄にいれるものは？

```go
package main

import "fmt"

type Color struct {
	Alpha uint8
	Red   uint8
	Green uint8
	Blue  uint8
}

[ 空欄 ] Hex() uint32 {
	return uint32(c.Alpha)<<24 |
		uint32(c.Red)<<16 |
		uint32(c.Green)<<8 |
		uint32(c.Blue)
}

func main() {
	mokeColor := Color{
		Alpha: 0xff,
		Red:   0x00,
		Green: 0xa3,
		Blue:  0x9e,
	}
	fmt.Printf("Hex=%08x\n", mokeColor.Hex())
}
```
