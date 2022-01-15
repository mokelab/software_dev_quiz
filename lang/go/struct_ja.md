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
