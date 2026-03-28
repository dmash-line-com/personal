# docs/voice/data.js のルール

## フォーマット

各レコードは以下のフィールドを持つオブジェクトで、すべてのフィールドは文字列型:

```js
{
  image: "images/YYYYMM-N.jpg",
  customer: "都道府県 姓様",
  name: "メーカー 車名",
  year: "YYYY年式",
  model: "グレード名",
  mileage: "N,NNN km",
  deliveryDate: "YYYY年M月",
  comment: "お客様の声の本文"
}
```

## ルール

- 配列名は `salesData`
- レコードは納車月の新しい順に並べる（同月内では image の番号が大きい順）
- 新しいレコードは配列の先頭に追加する
- すべてのフィールド値は文字列型（数値型にしない）
- mileage のカンマ区切りと末尾の ` km` を忘れないこと
