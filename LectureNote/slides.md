---
theme: default
title: Welcome to Slidev
highlighter: 'shiki'
lineNumbers: true
aspectRatio: 16/9
fonts:
  sans: BIZ UDPGothic
  serif: BIZ UDPMincho
  mono: Noto Sans Mono
layout: cover
---

# Slidev

これはカバーページです．

---

# Page 2

コードブロック

```ts
console.log('Hello, World!')
```

行のハイライト

```ts {2,3}
function add(
  a: Ref<number> | number,
  b: Ref<number> | number
) {
  return computed(() => unref(a) + unref(b))
}
```

```ts {2,3|5|all}
function add(
  a: Ref<number> | number,
  b: Ref<number> | number
) {
  return computed(() => unref(a) + unref(b))
}
```

```ts {monaco}
console.log('Hello, World!')
```


---

# このページはRed

<style>
  h1 {
    color: red
  }
</style>

ページタイトルのみが赤くなる

```html
<style>
  h1 {
    color: red
  }
</style>
```

---

# 次のスライドには適用されない

---

# 静的アセット

オンライン上の画像を読み込む方法
```markdown
![リモートの画像](https://sli.dev/favicon.png)
```

![リモートの画像](https://sli.dev/favicon.png)

---

# 静的アセット-2

ローカルのアセットについては`public`フォルダに格納し，頭にスラッシュをつけて参照します

これではできないなかった

```markdown
![ローカルの画像](./public/home.png)
```

![ローカルの画像](./images/home.png)

---

# 静的アセット-3

画像のサイズ調整をする場合 `<img>` タグを

```markdown
<img src="./images/home.png" class="m-40 h-40 rounded shadow" /> 
```

<img src="./images/home.png" class="m-40 h-40 rounded shadow" /> 


---

# スロット

レイアウトによっては，名前付きスロットを使用して，複数のコントリビューションポイントを提供できます．

例えば，`two-cols` レイアウトでは，左（`default`スロット）と右（`right`スロット）の2つのカラムを並べることができるようになります

フロントマターでレイアウトをしてどちらに記述するのかを指定します

```markdown
---
layout: two-cols
---

<template v-slot:default>

# Left

これは左側に表示されます．

</template>

<template v-slot:right>

# Right

これは右側に表示されます．

</template>

```

---
layout: two-cols
---

<template v-slot:default>

# Left

これは左側に表示されます．

</template>

<template v-slot:right>

# Right

これは右側に表示されます．

</template>