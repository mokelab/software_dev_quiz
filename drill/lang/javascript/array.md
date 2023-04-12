# 1. 配列の中身を全部表示してみる系

## 1-1

テストの点数が入っている配列scoresの中身を表示させてみてください。

```js
let scores = [75, 45, 30, 95, 62, 55]
// ここを書いてね
```

実行結果

```
75
45
30
95
62
55
```

<details><summary>回答例</summary>
```js
let scores = [75, 45, 30, 95, 62, 55]
for (let i = 0 ; i < scores.length ; i++) {
  console.log(scores[i])
}  
```
</detail>
  
  
