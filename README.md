# test-Slidev
 Slidevを使ってみる．

## 試してみる
公式サイトに従って試してみる．
https://ja.sli.dev/guide/why.html#%E8%A9%A6%E3%81%97%E3%81%A6%E3%81%BF%E3%82%8B

```shell
$ npm init slidev
```

npmはnode.jsのパッケージマネージャーです．なので，node.jsがないと使えません．

簡単に作成できた．

2回目以降は，プロジェクトフォルダに移動して起動する．

```shell
$ npm run dev
```

この場合，デフォルトの`slides.md`が対象となる．授業資料を想定しているのでmarkdownファイルを複数に分けたい．その時は，プロジェクトフォルダ内にmarkdownファイルを作成する（例：Lecture01.md）．このファイルを指定して起動する方法は以下の通りである．

```shell
$ npm run dev --- Lecture01.md
```

これで毎回授業に必要なMarkdownファイルを指定して起動すればOKとなる．以前は，1回の授業ごとにプロジェクトを作成していたが，この方法でかなり簡単にスライド作成ができるようになった．